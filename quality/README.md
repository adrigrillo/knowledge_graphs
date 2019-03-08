# Building and mining Knowledge Graphs
## Assignment 1
### Assessing the quality of a knowledge graph
A knowledge graph `graph.turtle` is given in the [Terse RDF Triple Language](https://www.w3.org/TR/turtle/) and is used
to assess its quality. To do so, the graph has to follow a given set of constrains that are established in the file
`schema.ShExC` that follow the specification of the [Shape Expressions Language](http://shex.io/shex-primer/).

The main objective of the constrains is to check if the graph follows the correct and expected data types and values and
that the formulation uses the best practices. Two different kind of constrains will be reviewed: RDF conformance
constrains, that will define the shape of the entities, and properties and data constrains.

#### RDF conformance constraints
- **Country**:
  - There should one shape definition for a Country.
  - Each Country should have the subject as an IRI.
  - Each Country should have a label using the property `rdfs:label`.
- **City**:
  - There should one shape definition for a ​City.
  - Each City should have the subject as an IRI.
  - Each City should have a label using the property `rdfs:label`.
- **Person**:
  - There should be one shape definition for a ​Person.
  - Each Person should have the subject as an IRI.
  - Each Person should be of type `schema:Person`.
- **Organisation**:
  - There should be one shape definition for an ​Organisation.
  - Each Organisation should have the subject as an IRI.
  - Each Organisation should be of type ​http://dbpedia.org/ontology/Organisation.

#### Properties and data type constraints
- **Country**:
  - Each ​Country​ should have a ​capital city​ and a ​population​ listed.
  - The capital city of each country should refer to a new shape - ​City​.
  - The data type for the population total of each country should be an appropriate data type from the XML 
    Schema Definition.
  - Each Country's label value should be of data type string from the 
    [XML Schema Definition](https://www.w3.org/2001/XMLSchema) (xsd:string).
- **City**:
  - Each ​City​ should have a property ​http://dbpedia.org/ontology/isCityOf.
  - The value of *isCityOf* should refer to a ​Country.
  - Each City's label value should be of data type string from the
    [XML Schema Definition](https://www.w3.org/2001/XMLSchema).
- **Person**:
  - Each ​Person​ should have a ​birth place​ and ​birth date​ property.
  - The birth place value should refer to a ​City​.
  - Each Person's birth date value should be of an appropriate data type from the
    [XML Schema Definition](https://www.w3.org/2001/XMLSchema).
- **Organisation**:
  - Each ​Organisation​ should have a property ​http://dbpedia.org/ontology/location​ and a 
  property ​http://dbpedia.org/ontology/foundedBy​ for it's founder.
  - Each ​Organisation​'s location value should conform to shape ​City.
  - The value of the foundedBy property should refer to a ​Person.