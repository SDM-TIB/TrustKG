# TrustKG
## A Framework for Knowledge Graphs based on Semantic Integration, Representation, and Curation of Scientific Data to enable Trustable and Interpretable Knowledge Exploration and Discovery

Data is a foundational asset for fostering a country’s economy and assuring citizens with a high-quality life. However, albeit recognized as pivotal infrastructures, global adoption of data-driven solutions is still lagging, particularly, in biomedicine. Thus, besides years of research in data integration, curation, and knowledge representation, the trustability of data-driven insights is still affected by the absence of interpretable methods to account for the correctness and bias in data-driven pipelines. 

In TrustKG, we aim at enabling explainable data integration in pipelines for transforming scientific data into semantically rich and linked knowledge graphs. TrustKG will be equipped with computational logic and ontologies to express temporality and causation relationships among ingested, curated, and integrated data. Further, TrustKG methods will resort to experts’ wisdom and computational techniques for validating and explaining data management decisions and outcomes. 

TrustKG is led by [Prof. Dr. Maria-Esther Vidal](https://www.tib.eu/en/research-development/research-groups-and-labs/scientific-data-management/staff/maria-esther-vidal) and supported by Leibniz Association in the program ["Leibniz Best Minds: Programme for Women Professors"](https://www.leibniz-gemeinschaft.de/en/research/leibniz-competition/leibniz-programme-for-women-professors), project 
[TrustKG-Transforming Data in Trustable Insights with grant P99/2020](https://www.leibniz-gemeinschaft.de/en/research/leibniz-competition/funded-projects).

## Knowledge Graphs and Knowledge-driven Ecosystems
Knowledge graphs (KGs) represent the convergence of knowledge and data as factual statements. KGs provide 
* Formal specifications for represening the meaning of entities, and their relationships and properties. 
* Taxonomic representations of entities, relationships, and classes
* Common understandings of a domain
* Inference processed to empower metadata and data with inference to deduce new facts

<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/KGraphs.png" width=60% height=60%>
 </p>

Data Ecosystems (DEs) are distributed, open, and adaptive information systems with the characteristics of being self-organized, scalable, and sustainable.
DEs are furnished with various computational methods to solve interoperability and integrate data, while preserving data privacy, security, and sovereignty. 

DEs can be further empowered with services that exploit the knowledge encoded in the meta-data and operators to satisfy business requirements, such as data transparency and traceability. These DEs are called [knowledge-driven data ecosystems](https://arxiv.org/abs/2105.09312). 

## The TrustKG Framework
Built on the concept of knowledge-driven ecosystems, the TrustKG framework represents a data ecosystem of heterogeneous data sources. 
Knowledge extracted from heterogeneous sources, e.g., clinical records, scientific publications, and pharmacologic data, is integrated into knowledge graphs. Ontologies describe the meaning of the combined data, and mapping rules enable the declarative definition of the transformation and integration processes. Moreover, the TrustKG framework is assessed in terms of the methods followed for data quality assessment and curation. Lastly, the role of controlled vocabularies and ontologies in data management is discussed and their impact on transparent knowledge extraction and analytics. The following figure illustrates the main components of the TrustKG framework. 

<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/GeneralTrustKG.png" width=60% height=60%>
 </p>


The TrustKG framework is applied in the context of the lung cancer pilots in the EU H2020 funded project [BigMedilytics](https://www.bigmedilytics.eu/), the ERA PerMed funded project [P4-LUCAT](https://p4-lucat.eu/), the EU H2020 projects [IASIS](https://project-iasis.eu/) and [CLARIFY](https://www.clarify2020.eu/), and  [ImProVIT](https://www.tib.eu/de/forschung-entwicklung/projektuebersicht/projektsteckbrief/improvit). Moreover, TrustKG has been used in the implementation of the [Knowledge4COVID-19] (https://github.com/SDM-TIB/Knowledge4COVID-19} knowledge graph. 


The TrustKG framework is also applied in the industry domain. 

<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/IndustrialData.png" width=80% height=80%>
 </p>

The TrustKG framework provides the basis to create an intelligent platform built on industry-wide value and supply chains in the context of [CoyPU](https://coypu.org/), a project funded by the German Federal Ministry for Economic Affairs and Climate Protection in the artificial intelligence innovation competition (BMWK). Lastly, TrustKG provides the basis for building the PLATOON knowledge graph in the context of the EU-funded H2020 project [PLATOON](https://platoon-project.eu/) with the aim to digitalize the energy sector, ad enable data exchange while ensuring privacy and sovereignty.


The following components compose the TrustKG framework platform, 
<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/SimplifyExtendedKGC-pipeline.png" width=100% height=100%>
 </p>

This video demonstrates these components in action [video](https://www.youtube.com/watch?v=6LLNpVa9fqk)

## Knowledge extraction and Linking Data
Scientific data is collected from different data sources; it is mainly characterized by the three dominant dimensions of the Vs model: volume-- very large data sets; variety-- sources in multiple data formats and models; and veracity-- data with potential biase, ambiguities, and noise. To overcome interoperability issues caused by data variety, knowledge extraction is performed to recognize entities and predicates from unstrcutured data. [FALCON](https://github.com/SDM-TIB/falcon2.0) performs entity and predicate recognition by linking surface forms in a short text into entities in KGs,e.g., UMLS, DBpedia, and Wikidata. It is guided by rules of English morphology, and tokenization and compounding Resorts to alignments among entities and labels in KGs for disambiguation. 
FALCON is available via an [API](https://labs.tib.eu/falcon/falcon2/). The techniques implemented in FALCON have been published in the following scientific publications:

Sakor A., Mulang I., Singh K., Shekarpour S., Vidal M.E., Lehmann J., Auer S. Old is Gold: Linguistic Driven Approach for Entity and Relation Linking of Short Text. NAACL-HLT  2019
Sakor A., Singh K., Patel A., Vidal. M.E. Falcon 2.0: An Entity and Relation Linking Tool over Wikidata. CIKM 2020

## Semantic Data Integration
The integration of the matching entities is performed over the knowledge graph by exploring concepts, relations, taxonomies, and rules represented in the knowledge graph. First, collected and curated big data is modeled using a unified schema and stored in a knowledge graph. Then, entity recognition and linking are employed for transforming textual values in the knowledge graph, e.g., descriptions and comments, into structured facts. Finally, different methods are combined to curate and complete the represented facts. 
Knowledge graph creation relies on mapping-driven algorithms guided by mapping rules that describe entities using a unified schema. Additionally, controlled vocabularies and ontologies used by the knowledge extraction tools are represented as RDF triples as well; links between these ontologies are also included in the knowledge graph to enable the identification of entities in different vocabularies. Similarity-based methods are performed for entity matching; similarity measures are able to exploit the knowledge encoded in the knowledge graph. Hybrid approaches combine reasoning processes on top of the knowledge graph with the wisdom of experts, and enable curation and knowledge completion. The mapping language RML is utilized to declaratively specify the process of semantic integration. The SDM-RDFizer is an RML compliant engine developed by the members of the Scientific Data Management group; it implements RML mapping rules with a set of non-blocking operators and is able to scale up the creation of large knowledge graphs. These techniques are implemented in the [SDM-RDFizer](https://github.com/SDM-TIB/SDM-RDFizer).

Mapping rules can also include knowledge extraction functions in addition to expressing  correspondences among data sources and a unified schema. Combining mapping rules and functions represents a powerful formalism to specify pipelines for integrating data into a knowledge graph transparently. EABlock is an approach integrating Entity Alignment (EA) as part of RML mapping rules. EABlock includes a block of functions performing entity recognition from textual attributes and link the recognized entities to the corresponding resources in Wikidata, DBpedia, and domain specific thesaurus, e.g., UMLS. EABlock provides agnostic and efficient techniques to evaluate the functions and transfer the mappings to facilitate its application in any RML-compliant engine. EABlock is publicly available [GitHub](https://github.com/SDM-TIB/EABlock).

The Semantic data integration techniques have been reported in the following publications: 

Maria-Esther Vidal, Kemele M. Endris, Samaneh Jazashoori, Ahmad Sakor, Ariam Rivas:
Transforming Heterogeneous Data into Knowledge for Personalized Treatments - A Use Case. Datenbank-Spektrum 19(2): 95-106 (2019) 

Jozashoori S., Vidal M.E. MapSDI: A Scaled-Up Semantic Data Integration Framework for Knowledge Graph Creation. OTM Conferences 2019

Chaves-Fraga D., Endris K., Iglesias E., Corcho O., Vidal M.E. What Are the Parameters that Affect the Construction of a Knowledge Graph? OTM Conferences 2019

Iglesias E., Jozashoori S., Chaves-Fraga D., Collarana D., Vidal M.E. SDM-RDFizer: An RML Interpreter for the Efficient Creation of RDF Knowledge Graphs. CIKM 2020

Jozashoori S., Chaves-Fraga D., Iglesias E., Vidal M.E., Corcho O. FunMap: Efficient Execution of Functional Mappings for Knowledge Graph Creation. ISWC 2020

Jozashoori S., Sakor A., Iglesias E., Vidal M-E. EABlock: A Declarative Entity Alignment Block for Knowledge Graph Creation Pipelines. SAC 2022

Enrique Iglesias, Samaneh Jozashoori, Maria-Esther Vidal: Scaling Up Knowledge Graph Creation to Large and Heterogeneous Data Sources. ["CoRR abs/2201.09694"](https://arxiv.org/abs/2201.09694) (2022).

## Research Data Management and FAIR Data principles
FAIR data principles emphasize the crucial role of machine-processable metadata to find, access, interoperate, and reuse data with minimal human intervention. Leibniz Data Manager is built on Semantic Web technologies to support researchers in documenting, analyzing, and sharing research datasets
<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/ArchitectureLDM.png" width=90% height=90%>
 </p>

 [Leibniz Data Manager](https://service.tib.eu/ldmservice/) solves interoperability across repositories and integrates datasets published in other repositories. 

Leibniz Data Manager has been reported in the following publication:

Anna Beer, Mauricio Brunet, Vibhav Srivastava, and Maria-Esther Vidal. Leibniz Data Manager -- A Research Data Management System. ESWC 2022 Poster and Demos.

The open [demo](https://service.tib.eu/ldmservice/demo) illustrates the main features of LDM. 
## Federated Query Processing
[DeTrusty](https://github.com/SDM-TIB/DeTrusty) is a SPARQL federated query engine with the focus on the explainability and trustworthiness of the query result.

<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/VirtualDIS.png" width=70% height=70%>
 </p>


## SHACL Validation
[Trav-SHACL](https://github.com/SDM-TIB/Trav-SHACL) is a SHACL engine capable of planning the traversal and execution of a shape schema in a way that invalid entities are detected early and needless validations are minimized. Trav-SHACL reorders the shapes in a shape schema for efficient validation and rewrites target and constraint queries for fast detection of invalid entities.

Trav-SHACL has been reported in the following publication: 

Mónica Figuera, Philipp D. Rohde, and Maria-Esther Vidal. Trav-SHACL: Efficiently Validating Networks of SHACL Constraints. The Web Conference (WWW 2021). (https://doi.org/10.1145/3442381.3449877)


## Analytics and Prediction
Statistical and predictive methods are defined on top of the knowledge graph. Predictive problems include; Impact of drug-drug interactions in survival time, classification of patients. These methods are enhanced with contextual knowledge represented in the knowledge graph with the aim of identifying accurate predictions whose meaning can be described. 
InterpretME is a tool for fine-grained representations, in a knowledge graph, of the main characteristics of trained machine learning models. InterpretME traces metadata at dfferent stages of a predictive modeling pipeline.

<p align="center">
<img src="https://github.com/SDM-TIB/TrustKG/blob/main/images/ML%20pipelineAnnotated.png" width=50% height=50%>
 </p>
 
The traced metadata includes features' definition and SHACL validation, and model-based characteristics (e.g., relevant features, and interpretations of prediction probabilities and model decisions). InterpretME allows for the definition of a model's features over knowledge graphs; SHACL states domain integrity constraints. Moreover, InterpretME traces the steps of data collection, curation, integration, and prediction, and documents the collected metadata in a knowledge graph. 


InterpretME is publicly available at  [GitHub](https://github.com/SDM-TIB/InterpretME) and [Zenodo](https://doi.org/10.5281/zenodo.6523740).

## Where is the TrustKG framework used
- [iASiS](http://project-iasis.eu/): big data for precision medicine, based on patient data insights. The iASiS RDF knowledge graph comprises more than 1.2B RDF triples collected from more than 40 heterogeneous sources using over 1300 RML triple maps. 
- [BigMedilytics](https://www.bigmedilytics.eu/): lung cancer pilot. 800 RML triple maps are used to create the lung cancer knowledge graph from around 25 data sources with 500M RDF triples.
- [CLARIFY](https://www.clarify2020.eu/): predict poor health status after specific oncological treatments
- [P4-LUCAT](https://www.tib.eu/de/forschung-entwicklung/projektuebersicht/projektsteckbrief/p4-lucat)
- [ImProVIT](https://www.tib.eu/de/forschung-entwicklung/projektuebersicht/projektsteckbrief/improvit)
- [EUvsVirus Hackathon (April 2020)](https://blogs.tib.eu/wp/tib/2020/05/06/how-do-knowledge-graphs-contribute-to-understanding-covid-19-related-treatments/). SDM-RDFizer created the Knowledge4COVID-19 knowledge graph during the participation of the team of the Scientific Data Management group. By June 7th, 2020, this KG is comprised of 28M RDF triples describing at a fine-grained level 63527 COVID-19 scientific publications and COVID-19 related concepts (e.g., 5802 substances, 1.2M drug-drug interactions, and 103 molecular disfunctions
- [PLATOON](https://platoon-project.eu/) to generate a knowledge graph that comprises 80,762,377 resources described in terms of 220,204,301 RDF triples. The resources are part of 162 classes of the PLATOON Semantic data models. 
- [CoyPU](https://coypu.org/) to generate a platform that enables high-quality, up-to-the-minute insights into economic facts, trends, impact relationships, and forecasts.



