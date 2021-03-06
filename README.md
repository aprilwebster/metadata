# metadata

## what is metadata

## a history


## metadata standards
- to be useful and understandable, metadata must be standardized to provide a common language with semantics that are as clearly defined (and unambiguous) as possible
- without a common language, integration and interoperability are not possible
- XML is the language of choice for most industry standards due to its semi-structured nature which provides a way to organize properties and facilitate easier analysis and comparison, while still providing support for unstructured data

### general purpose standards
- **[Dublin Core Metadata Element Set (DCE)](http://www.dublincore.org/specifications/dublin-core/dcmi-terms/ )**: general description of resources that's limited to basic data including author, format, language, id or title.  Registered as ISO Standard 15836 in 2009.
   - can think of this as the basic standard for metadata
   - benefits: simple, easy-to-understand, easy-to-collect
- **[W3C MLSchema](http://ml-schema.github.io/documentation/ML%20Schema.html)**: 


### industry standards
- many industries have come up with solutions in the form of standards and schemas for recording metadata to provide information to end users for datasets and models
- it would be wise for the ML domain to look into the state of the art for metadata management in other domains that have been addressing these issues over the past few decades.  Metadata to help end users understand and evaluate appropriate usage and handle bias have already been baked into metadata standards in these domains.

### issues with standards
- can be inflexible
- standards creep
- TODO: include journal paper on xml standards mgmt call-to-action

## gis domain (1992 - present)
- FGDC metadata standard to describe geospatial datasets dates back to at least 1992
   - https://web.archive.org/web/20061018013240/http://libraries.mit.edu/guides/subjects/metadata/standards/fgdc.html
- Other references:
   - http://desktop.arcgis.com/en/arcmap/10.3/manage-data/metadata/a-quick-tour-of-creating-and-editing-metadata.htm#ESRI_SECTION1_CC2F6DEED69B428D8C694D2804F00640
   - http://desktop.arcgis.com/en/arcmap/latest/manage-data/metadata/illustrated-guide-to-complete-fgdc-metadata.htm#GUID-16DC4914-3953-405B-BFEC-555C129961F3
   - https://www.fgdc.gov/resources/factsheets/documents/GeospatialMetadata-July2011.pdf
   - https://www.fgdc.gov/metadata/documents/ValueOfMetaFiles/ValueOfMetaPDF

## data management domain
- 1997: https://www.cs.waikato.ac.nz/~ml/publications/1997/Cunningham-Cataloging97.pdf

### [goods](http://sites.computer.org/debull/A16sept/p5.pdf) (Alon Halevy at Google Research) - 2016
- addresses the issue of the challenge of dataset metadata generation
- instead of a requiring metadata authoring at the time of dataset creation, Halevy proposes a decentralized approach to crawling metadata after-the-fact from datasets that are already in use
- system for managing data lakes, aka a 'collection of datasets that often are not well organized or not organized at all and where one needs to "fish" for useful datasets'
- other references
   - https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45390.pdf

## machine learning industry (2018 - present)
- this is not a new concept, but the ML domain is struggling with how to manage with the explosion of ML models and datasets in the ML wild west, particularly under the pressure of the lashback regarding bias and accountability

### [model cards](http://delivery.acm.org/10.1145/3290000/3287596/p220-Mitchell.pdf?ip=170.225.9.141&id=3287596&acc=NO%20RULES&key=4D4702B0C3E38B35%2E4D4702B0C3E38B35%2ED2E531DB056F4A45%2E4D4702B0C3E38B35&__acm__=1556846985_823be4d723bed277a13ad2335eecd8d8) (Google + U of T) - January 2019
- general concepts and a framework for what metadata is necessary to clarify the intended usage of ML models
- NOT an actual machine-readable implementation/schema 
- good starting point for identification of what information is useful, but will require a machine-readable definition to become truly useful

### [datasheets for datasets](https://arxiv.org/pdf/1803.09010.pdf) (Google + Microsoft Research + AI Now + universities) - April 2019
- "motivation, composition, collection process, recommended uses"
- creation, distribution, and maintenance process
- provide a set of questions covering the information that a datasheet for a dataset might contain, they are not intended to be prescriptive
- propose a reflective and manual process of creation, not automated to avoid the pitfalls

### [factsheets for datasets](https://www.ibm.com/blogs/research/2018/08/factsheets-ai/) (IBM) - February 2019 (August 2018)
- IBM refers to this sort of metadata as a 'Supplier's Declaration of Conformity (SDoC)'
- similar to Google/Microsoft's concept of a datasheet, it prescribes dataset metadata categories and questions for each that the supplier of the dataset should provide
- goal of the factsheet is to address concerns over fairness, explainability, bias, etc

### [data statements](https://www.mitpressjournals.org/doi/abs/10.1162/tacl_a_00041) (U of W) - 2018
- more ethically responsive models
- mitigating bias

### [dataset nutrition label framework](tba)
- it's nice to see basic descriptive statistics addressed in this framework, something that seems to be lacking in the ML domain

### [factsheets](https://arxiv.org/pdf/1808.07261.pdf)
- FactSheets: Increasing Trust in AI Services through Supplier's Declarations of Conformity  (August 2018)
```
Accuracy is an important concern for suppliers of artificial intelligence (AI) services, but considerations beyond accuracy, such as safety (which includes fairness and explainability), security, and provenance, are also critical elements to engender consumers' trust in a service. Many industries use transparent, standardized, but often not legally required documents called supplier's declarations of conformity (SDoCs) to describe the lineage of a product along with the safety and performance testing it has undergone. SDoCs may be considered multi-dimensional fact sheets that capture and quantify various aspects of the product and its development to make it worthy of consumers' trust. Inspired by this practice, we propose FactSheets to help increase trust in AI services. We envision such documents to contain purpose, performance, safety, security, and provenance information to be completed by AI service providers for examination by consumers. We suggest a comprehensive set of declaration items tailored to AI and provide examples for two fictitious AI services in the appendix of the paper.
```
