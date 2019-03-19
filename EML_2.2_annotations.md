# Semantic Annotations in EML 2.2

## O’Brien, Chong, Schildhauer 
## Databits 2019 Spring

# Introduction
A semantic annotation involves the attachment ("annotation") of semantic metadata to a resource -- which in this 
context is an EML element. A semantic annotation provides a pointer to useful descriptions, definitions, or relationships 
in a computer-usable way. The process of creating semantic annotations may seem tedious, but the payoff is vastly enhanced 
information discovery and interpretation. Semantic annotations will make it easier for others to find, reuse and credit data.

Annotations are most powerful when they reference terms from web-accessible knowledge graphs called "ontologies" that 
can be traversed by computer logic. Hence, semantic statements must be logically consistent; they are not simply a set 
of loosely structured keywords. Inconsistent annotations create confusion, and so constructors should take care, and bring 
up questions for feedback.

# Semantic Triples
Semantic annotations enable the creation of what are called triples, or 3-part statements conforming to the W3C recommended 
RDF data model (____REF___). The three parts of a triple are a subject, a predicate and an object. 

```
[subject] [predicate] [object]
```

These components are analogous to parts of a sentence: the subject and object can be thought of as nouns in the 
sentence and the predicate (sometimes called “object property” or “data property”) is akin to the verb or a relationship 
that connects the subject and object. The semantic triple expresses a statement about the associated resource, the subject.

The three components of a semantic triple should be HTTP URIs (uniform resource identifiers), which are 
globally unique and persistent (unchanging), and resolvable or dereferenceable 

RDF is not designed for being displayed to people. It is designed so that components are accessible through the Web, 
for computers to look up precise definitions and relationships between these resources and other concepts. The simplest 
triple statement is a sequence of (subject, predicate, object) terms, separated by whitespace and terminated by '.' (
W3C ref). Example 1 expresses the relationship between Spiderman and the Green Goblin, with fake URIs:

Example 1
```
<http://example.org/#spiderman> <http://example.org/#enemyOf> <http://example.org/#green-goblin> .
```

Example 2 is a true triple created for a Jornada LTER dataset. The URIs resolve, saying that a dataset (subject) was 
"located in" (predicate/property) a "desert area" (object/value). The subject dereferences to a dataset in PASTA, 
knb-lter-jrn.210327001.1, the predicate to a relationship ontology, and the object to a concept in the Environment 
Ontology, which has a complex definition of “desert area”. 

Example 2
```
<https://doi.org/10.6073/pasta/06db7b16fe62bcce4c43fd9ddbe43575> <http://purl.obolibrary.org/obo/RO_0001025> <http://purl.obolibrary.org/obo/ENVO_00000097> .
```

The “located in” relationship means that more precise searches can be constructed, e.g. a computer can return this 
dataset alongside other datasets that are "located in" a precisely defined area called a "desert" -- not just related 
to deserts in some unknown way, which is all that is possible with keywords. 

# Semantic Annotations in EML

Continuing with the JRN example, the annotation in EML looks like this 

Example 3 jrn dataset-level anntation





# EML Annotations to Semantic Triples
The subjects of triples generated from EML annotations will likely be HTTP URI's that identify the parent element of 
the annotation, e.g, dataset resource itself or a specific data entity attributes. The objects of EML semantic annotations, 
as well as the predicates that relate the subject to the object, will most typically be HTTP URI references to terms in 
controlled vocabularies (also called "knowledge graphs", or "ontologies") accessible through the Web, so that users 
(or computers) can dereference the URI's and look up precise definitions and relationships of these resources to other 
terms.




# Section 4
Lorem ipsum



# References
Lorem ipsum

learn more: https://www.w3.org/TR/rdf11-primer/). 

Ref for example spiderman https://www.w3.org/TR/turtle/




