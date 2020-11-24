**Download the File Dataset from Film Corpus 2.0**

website: https://nlds.soe.ucsc.edu/fc2

Note: input your information then you can download it.

**Processing (steps):**

1. Use Stanford CoreNLP 3.5.2 to tokenize, lemmatize, POS tag, dependency parse and label named entities. [[1]](#1)
   1. NLTK since version 3.2.3 has a new interface to Stanford CoreNLP using the StanfordCoreNLPServer: nltk.parse.corenlp.CoreNLPParser. You should avoid using the
   Stanford tokenizer/segmenter/NER from nltk.tokenize and nltk.tag (unless stuck on a very old version of NLTK) – these classes are very slow, since they perform
   calls to Java via the command-line for each invocation.
   
1. Extract events by keeping all tokens whose POS tags begin with VB: VB, VBD, VBG, VBN, VBP, and VBZ.
1. Exclude light verbs e.g. be, let, do, begin, have, start, try, be- cause they often only represent a meaningful event when combined with their complements.
1. extract the subject (nsubj, agent), direct object (dobj, nsubjpass), indirect object (iobj) and particle of the verb (compound:prt)
1. In order to abstract and merge different arguments, eneralize the arguments to two types: person and something.
   1. its named entity type is PERSON; or 
   1. it is a pronoun (except “it”); or 
   1. it is a noun in WordNet with more than half of its Synsets hav- ing lexical filename noun.person, e.g. doctor, soldier, waiter, man, woman. 
   1. if we could generalize over other types of named entities as well is better, such as location. But Stanford NER identifi- able named entities rarely occur in film data.
1. record the combinations of its arguments and particle for every instance. For example, the instance of event “pick” in sentence: He picked it up... a pearl, has combination subj: person, dobj: something, iobj: none, particle: up. pick the combination with the highest frequency to represent the arguments and particle for each event.
   
   
## References

<a id="1">[1]</a> Christopher D Manning, Mihai Surdeanu, John Bauer, Jenny Rose Finkel, Steven Bethard, and David Mc- Closky. 2014. The Stanford CoreNLP natural lan- guage processing toolkit. In ACL (System Demon- strations). pages 55–60.
