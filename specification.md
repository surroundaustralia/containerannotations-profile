# Container Annotations Specification
This document specifies the rules that [RDF](https://www.w3.org/RDF/) data must adhere to, to be valid according to this profile.

This document's persistent identifier is:

* <https://w3id.org/profile/contanno/spec>

Note that this profile is evvectively the opposite to the [Members Profile](https://w3id.org/profile/mem/spec) that requires that only containers' members be present - no annotations.

## Role
This document is part of the larger Container Annotations Profile which contains multiple parts: this specification, validators and so on. The profile is online at:

* <https://w3id.org/profile/contanno>

Only the human-readable requirements specified by this specification are listed here. They do correspond to machine-executable RDF validation tests supplied by this profile in the [Shapes Constraint Language (SHACL)](https://www.w3.org/TR/shacl/)-conformant validation resource:

* <https://w3id.org/profile/contanno/validator>

Tools such as [pySHACL](https://github.com/RDFLib/pySHACL) and the [SHACL Playground](https://shacl.org/playground/) can be used with the validator file to test instance data. This Spec should be used, by people, to understand the tests.

## Requirements
This specification places requirements on a number of known [OWL](http://www.w3.org/TR/owl2-primer/)/[RDFS](http://www.w3.org/TR/rdf-schema/) classes that are forms of containers. In all cases the requirements specify that, when viewed according to this profile, annotation and data properties of the container class instance must be shown but not the member indicating properties. For the basic RDFS class `Container` that means any property other than `rdfs:member`, for SKOS' `ConceptScheme` all properties other than `skos:inScheme` or derived properties, etc.

### General Requirement

* **Requirement General**:
    * For each container instance, predicates indicating parts (members) of it _MUST NOT_ be present.

Specific container classes and their properties to exclude are given as individual Requirements next. These translate directly to validation rules in [this profile's validator](https://w3id.org/profile/contanno/validator)

* **Requirement RDFS**:
    * For each RDFS `Container` instance, predicates indicating parts of it, such as RDFS' `member` _MUST NOT_ be present.

* **Requirement RDF**:
    * For each RDF `Bag`, `Alt` or `Seq` instance, predicates indicating parts of it, such as RDFS' `member` _MUST NOT_ be present.

* **Requirement DCAT**:
    * For each DCAT `Catalog` instance, predicates indicating parts (members) of it _MUST NOT_ be present. These include `dcterms:hasPart` and any subproperties of it, in particular those listed in DCAT: `dcat:catalog`, `dcat:dataset` & `dcat:service`.

* **Requirement DCTERMS**:
    * For each Dublin Core Terms `Collection` instance, predicates indicating parts of it, such as Dublin Core Terms `hasPart` or RDFS' `member` _MUST NOT_ be present.

* **Requirement GeoSPARQL**:
    * For each GeoPSARQL `SpatialObjectCollection`, `FeatureCollection` or `GeometryCollection` instance, predicates indicating parts of it, such as RDFS' `member` or ublin Core Terms `hasPart` _MUST NOT_ be present.

* **Requirement SKOS**:
    * For each SKOS `ConceptScheme`, `Collection` or `OrderedCollection` instance, predicates indicating parts of it, such as SKOS' `hasTopConcept`, `member` or `memberList` _MUST NOT_ be present.


## Profile expansion

This profile indicates a general requirement and exemplifies that requirement for 6 ontologies. It may be expanded to include other specific examples if users so wish.

Please send any change requests to the profile contacts listed in the [profile guidance README](https://w3id.org/profile/contanno/guidance) and/or submit issues to [this profiles' repository](https://w3id.org/profile/contanno/repo).
