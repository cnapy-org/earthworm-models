# earthworm-models
Metabolic models of the earthworm species *Lumbricus rubellus* and *Lumbricus terrestris*. The models are created from BioCyc PGDBs which are set up in the first step 
with [PathwayTools](https://pathwaytools.com/) using its PathoLogic component. The input for this is created with the create_biocyc_input.ipynb notebook.
The initial models are created with the MetaFlux component of PathwayTools using the provided SBML_export.fba files. After this the get_MetaNetX_annotations.ipynb
notebook needs to be executed to collect metabolite annotations which are then integrated into the models with the preprocess_MetaFlux_SBML.ipynb notebook. Finally
the use_icel_compartments_for_metabolic_model.ipynb notebook created the fully compartmentalized models. The latter are included in this repository and can be found under 
lumbricus_rubellus/metabolic_model/LRU1.sbml and lumbricus_rubellus/metabolic_model/LRT1.sbml respectively.

## Installation:
Clone the repository, go into the earthworm-models directory and install into your current Python environment with:

pip install .

Tip: If you use the -e option during installation then updates from a 'git pull' are at once available in your Python envrionment without the need for a reinstallation.


