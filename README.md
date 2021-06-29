# Container Annotations Profile
This is a profile of fundamental Semantic Web data models that characterise containers - objects that expect to have other objects as their members - that describes an _annotations only_ view of the container, that is a veiw of the container object's properties other than its members.

The purpose of this profile is to specify a view of containers that allow users of them to understand their annotations and simple data values separately from the list of container's members. Sometimes it is necissary to know about the container without its, potentially large, list of members getting in the way.

Note that this profile is evvectively the opposite to the [Members Profile](https://w3id.org/profile/mem) that requires that only containers' members be present - no annotations.

This profile defines _requirements_ for data wanting to conform to it in a _Specification_ document and provides some data validators in a Shapes Validation Language (SHACL) file that can be used to conformance test data.


## Profile applicability

This profile applies to any object - class instance - that can conventionally be conceived of as being a _container_ that is, an object designed primarily to contain other objects, it's members. This starts with the [RDFS Schema's](http://www.w3.org/TR/rdf-schema/) `Container` and may apply to any specialisation of it or similarly designed class, such as:

* [RDF's](http://www.w3.org/TR/rdf11-concepts/) `Bag`, `Seq` & `Alt` classes
* [DCAT's](https://www.w3.org/TR/vocab-dcat/) `Catalog` class
* [Dublin Core Terms'](https://dublincore.org/specifications/dublin-core/dcmi-terms/) `Collection` class
* [GeoSPARQL 1.1's](https://opengeospatial.github.io/ogc-geosparql/geosparql11/spec.html) `FeatureCollection` class
* [SKOS'](https://www.w3.org/TR/skos-reference/) `ConceptScheme` & `Collection` classes 

This profile is hosted online in [Linked Data](https://www.w3.org/standards/semanticweb/data) form using a persistent web address:

* <https://w3id.org/profile/contanno>


## License  
This code is licensed using the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) licence. See the [LICENSE file](LICENSE) for the deed. 

Note [Citation](#citation) below for attribution.


## Citation
To cite this profile, please use the following (formulated in [BibTex](http://www.bibtex.org/)):

```
@software{ogcldapi-profile,
  author = {{SURROUND Australia Pty Ltd}},
  title = {{Container Annotations Profile}},
  version = {1.0},
  date = {2021},
  publisher = {{SURROUND Australia Pty Ltd}},
  url = {https://w3id.org/profile/contanno}
}
``` 


## Contact
*publisher:*  
![](style/SURROUND-logo-100.png)  
**SURROUND Australia Pty. Ltd.**  
<https://surroundaustralia.com>  

*creator:*  
**Dr Nicholas J. Car**  
*Data Systems Architect*  
SURROUND Australia Pty. Ltd.  
<nicholas.car@surroudaustralia.com>  
<https://orcid.org/0000-0002-8742-7730>
