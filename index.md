---
title: Overview
layout: page
---

## Just Enough Results Model (JERM)

### Overview

The JERM provides a framework to describe SEEK assets and the relationships between assets and the experiments that created them. 
Crucially, all assets are related to the scientists that created them and the projects they originate from, 
so the model captures provenance information as well as physical links between assets. 
JERM definitions for each type of data in SEEK is different, but highly overlapping and they comply with existing [MIBBI](http://www.biosharing.org/standards/mibbi) guidelines where they are available.

The JERM describes what type of experiment was performed, who performed it, and what was measured. 
These elements are common to all data types in Systems Biology, 
but each data type (e.g. microarray, mass spectrometry, enzymatic reactions), requires a different set of additional metadata. 
For enzyme experiments, the reactions being catalyzed need to be recorded, with substrates, products, and details of inhibition. 
For microarray experiments, the methods for quality control and normalization of the data should be recorded. 
For proteomics or metabolomics with mass spectrometry, detailed descriptions of the instruments are required. 
For all cases, however, a description of the biological samples and any treatments applied is essential in order to understand 
the results of the experiment.

### JERM Ontology

![JERM Ontology Classes]({{ site.baseurl }}/images/jerm2_ontology_classes.png "Classes"){: .ontology_classes .pic}

The [JERM Ontology](https://bioportal.bioontology.org/ontologies/JERM) is an application ontology designed to describe the items in SEEK and the relationships between them 
(for example, data, models, experiment descriptions, results, samples, protocols, standard operating procedures and publications); 
and to enable these relationships to be expressed with formal semantics. 
It is based on the idea of the Minimal Information Model. 
A Minimum Information Model is the smallest amount of metadata required in order to make experimental data discoverable and 
interpretable by other scientists. Minimum Information Models have recently gained popularity in the Life Sciences because 
they offer a pragmatic solution to the provision of sufficient metadata. 
Metadata annotation is both time-consuming and costly, and the biggest benefits are not for the data producers, 
but for scientists wishing to reuse data.

Most Minimum Information Models exist as checklists, or XML specifications (XML schemas). There are already over 50, 
which have been collected under the umbrella of MIBBI (Minimum Information for Biological and Biomedical Investigations). 
The JERM takes the specification one step further, expressing the minimum information model as an [OWL ontology](http://en.wikipedia.org/wiki/Web_Ontology_Language).

Currently, the JERM ontology contains approximately 295 classes and 50 properties. 
It is represented in OWL in order to capture rich associations between SEEK assets and to allow complex queries and reasoning. 
The terms and properties of the JERM ontology therefore provide a schema for managing and extracting SEEK metadata.

Using the JERM ontology to describe SEEK assets, and representing them in [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework), 
is essential to the sustainability of the resource. 
Data produced using continuously developed new experimental techniques must be incorporated into the SEEK. 
The flexibility and extensibility of RDF is ideal for such conditions. Using the JERM framework means that adding a new data type is possible without requiring the re-design of the underlying data model. Any new data type would have the same set of minimal metadata elements, plus some elements specific to that data. This would allow aggregation at any point of commonality (for example, the biological samples, the same factors studied, or membership of the same study), but the fact that there are differences between datasets is an advantage and not a complication.

To access a latest version of the JERM ontology, or if you wish to be involved in its development and make contributions, 
please visit our [JERM Ontology GitHub Repository](https://github.com/FAIRdom/JERMOntology).

### JERM Templates and RightField

An OWL ontology, however, is not a suitable representation for laboratory biologists. 
The JERM schemas must be presented in a way that enables their use, 
without requiring the Systems Biologists to invest time and resources in learning new tools and ontology/RDF skills.

![RightField]({{ site.baseurl }}/images/rightfield-jerm-template.png "RightField"){: .rightfield_template .pic}

The majority of laboratory scientists (microbiologists, biochemists, 
molecular biologists, and geneticists) use spreadsheets for the daily management and manipulation of data. 
By embedding the JERM metadata model in a spreadsheet format, and enabling the use of JERM (and other) vocabulary terms for annotation, 
the process of standardized semantic data collection can become part of the existing data management activities in the laboratory. 
JERM-compliance in SEEK is therefore achieved by the sharing of JERM-compliant spreadsheet templates.

To allow us to embed ontologies into spreadsheets, and enforce the use of semantic controlled vocabularies, 
without the overhead of understanding semantics or ontologies, we developed [RightField](http://www.rightfield.org.uk/). We call this Semantic annotation by Stealth. RightField is a general tool for embedded semantic terms into spreadsheet templates, and isn't specifically restricted to the JERM.

JERM spreadsheet templates have been developed for a wide range of experimental data types. In collaboration with members of the SysMO consortium, templates have been designed for numerous different types of microarray and RNA-Seq data, proteomics, interactomics, metabolomics, and enzyme kinetics.