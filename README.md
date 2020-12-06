# Medical-Knowledge-Graph
An ecosystem of knowledge driven tools for the transformation of scientific data into a medical knowledge graph. It transforms and integrates heterogeneous data into knowledge graphs. The following figure illustrates the main components of the Medical Knowledge Graph platform.
![Medical Knowledge Graph Platform](https://github.com/SDM-TIB/Medical-Knowledge-Graph/blob/main/images/GeneralKGCreation.png "Medical Knowledge Graph Platform") 

The Medical Knowledge Graph Platform has been reported in the following scientific article: 

Maria-Esther Vidal, Kemele M. Endris, Samaneh Jazashoori, Ahmad Sakor, Ariam Rivas:
Transforming Heterogeneous Data into Knowledge for Personalized Treatments - A Use Case. Datenbank-Spektrum 19(2): 95-106 (2019) 

The following components compose the Medical Knowledge Graph platform.  

# Knowledge extraction and Linking Data
Scientific data is collected from different data sources; it is mainly characterized by the three dominant dimensions of the Vs model: volume-- very large data sets; variety-- sources in multiple data formats and models; and veracity-- data with potential biase, ambiguities, and noise. To overcome interoperability issues caused by data variety, knowledge extraction is performed to recognize entities and predicates from unstrcutured data. FALCON https://github.com/SDM-TIB/falcon2.0) performs entity and predicate recognition by linking surface forms in a short text into entities in Knowledge Graphs (KGs),e.g., UMLS, DBpedia, and Wikidata. It is guided by rules of English morphology, and tokenization and compounding Resorts to alignments among entities and labels in KGs for disambiguation. 
FALCON is available via an API (https://labs.tib.eu/falcon/falcon2/). The techniques implemented in FALCON have been published in the following scientific publications:

Sakor A., Mulang I., Singh K., Shekarpour S., Vidal M.E., Lehmann J., Auer S. Old is Gold: Linguistic Driven Approach for Entity and Relation Linking of Short Text. NAACL-HLT  2019
Sakor A., Singh K., Patel A., Vidal. M.E. Falcon 2.0: An Entity and Relation Linking Tool over Wikidata. CIKM 2020

# Semantic Data Integration
The integration of the matching entities is performed over the knowledge graph by exploring concepts, relations, taxonomies, and rules represented in the knowledge graph. First, collected and curated big data is modeled using a unified schema and stored in a knowledge graph. Then, entity recognition and linking are employed for transforming textual values in the knowledge graph, e.g., descriptions and comments, into structured facts. Finally, different methods are combined to curate and complete the represented facts. 
Knowledge graph creation relies on mapping-driven algorithms guided by mapping rules that describe entities using a unified schema. Additionally, controlled vocabularies and ontologies used by the knowledge extraction tools are represented as RDF triples as well; links between these ontologies are also included in the knowledge graph to enable the identification of entities in different vocabularies. Similarity-based methods are performed for entity matching; similarity measures are able to exploit the knowledge encoded in the knowledge graph. Hybrid approaches combine reasoning processes on top of the knowledge graph with the wisdom of experts, and enable curation and knowledge completion. The mapping language RML is utilized to declaratively specify the process of semantic integration. The SDM-RDFizer is an RML compliant engine developed by the members of the Scientific Data Management group; it implements RML mapping rules with a set of non-blocking operators and is able to scale up the creation of large knowledge graphs. The techniques implemented in the SDM-RDFizer (https://github.com/SDM-TIB/SDM-RDFizer) have been reported in the following publications: 

Jozashoori S., Vidal M.E. MapSDI: A Scaled-Up Semantic Data Integration Framework for Knowledge Graph Creation. OTM Conferences 2019

Chaves-Fraga D., Endris K., Iglesias E., Corcho O., Vidal M.E. What Are the Parameters that Affect the Construction of a Knowledge Graph? OTM Conferences 2019

Iglesias E., Jozashoori S., Chaves-Fraga D., Collarana D., Vidal M.E. SDM-RDFizer: An RML Interpreter for the Efficient Creation of RDF Knowledge Graphs. CIKM 2020

Jozashoori S., Chaves-Fraga D., Iglesias E., Vidal M.E., Corcho O. FunMap: Efficient Execution of Functional Mappings for Knowledge Graph Creation. ISWC 2020

# Analytics and Prediction
Statistical and predictive methods are defined on top of the knowledge graph. Predictive problems include; Impact of drug-drug interactions in survival time, classification of patients. These methods are enhanced with contextual knowledge represented in the knowledge graph with the aim of identifying accurate predictions whose meaning can be described. 


# Projects where the Medical Knowledge Graph Platform has been used
- iASiS (http://project-iasis.eu/): big data for precision medicine, based on patient data insights. The iASiS RDF knowledge graph comprises more than 1.2B RDF triples collected from more than 40 heterogeneous sources using over 1300 RML triple maps. 
- BigMedilytics (https://www.bigmedilytics.eu/): lung cancer pilot. 800 RML triple maps are used to create the lung cancer knowledge graph from around 25 data sources with 500M RDF triples.
- CLARIFY (https://www.clarify2020.eu/): predict poor health status after specific oncological treatments
- P4-LUCAT (https://www.tib.eu/de/forschung-entwicklung/projektuebersicht/projektsteckbrief/p4-lucat)
- ImProVIT (https://www.tib.eu/de/forschung-entwicklung/projektuebersicht/projektsteckbrief/improvit)
- PLATOON (https://platoon-project.eu/) 
- EUvsVirus Hackathon (April 2020) (https://blogs.tib.eu/wp/tib/2020/05/06/how-do-knowledge-graphs-contribute-to-understanding-covid-19-related-treatments/). SDM-RDFizer created the Knowledge4COVID-19 knowledge graph during the participation of the team of the Scientific Data Management group. By June 7th, 2020, this KG is comprised of 28M RDF triples describing at a fine-grained level 63527 COVID-19 scientific publications and COVID-19 related concepts (e.g., 5802 substances, 1.2M drug-drug interactions, and 103 molecular disfunctions


