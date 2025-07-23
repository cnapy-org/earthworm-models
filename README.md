# earthworm-models
Metabolic models of the earthworm species *Lumbricus rubellus* and *Lumbricus terrestris*. The models are created from [BioCyc](https://biocyc.org/) PGDBs which are set up in the first step 
with [PathwayTools](https://pathwaytools.com/) 29.0 using its PathoLogic component. The input for this is created with the create_biocyc_input.ipynb notebook. Note that this process cannot be fully automated and requires several user actions as described in the notebook. In particular some experience with PathwayTools can be very helpful. The PGDBs can be accessed at [LumbriCyc](https://lumbricyc.mpi-magdeburg.mpg.de/), downloaded via Zenodo or if you have PathwayTools installed via its Registry.

The initial metabolic models are created with the MetaFlux component of PathwayTools using the [lumbricus_rubellus/MetaFlux/SBML_export.fba](https://github.com/cnapy-org/earthworm-models/blob/master/lumbricus_rubellus/MetaFlux/SBML_export.fba) and [lumbricus_terrestris/MetaFlux/SBML_export.fba](https://github.com/cnapy-org/earthworm-models/blob/master/lumbricus_terrestris/MetaFlux/SBML_export.fba) files. After this, the get_MetaNetX_annotations.ipynb
notebook needs to be executed to collect metabolite annotations which are then integrated into the models with the preprocess_MetaFlux_SBML.ipynb notebook. Finally
the use_icel_compartments_for_metabolic_model.ipynb notebook creates the fully compartmentalized models. The latter are included in this repository and can be found under 
[lumbricus_rubellus/metabolic_model/LRU1.sbml](https://github.com/cnapy-org/earthworm-models/blob/master/lumbricus_rubellus/metabolic_model/LRU1.sbml) and [lumbricus_terrestris/metabolic_model/LRT1.sbml](https://github.com/cnapy-org/earthworm-models/blob/master/lumbricus_terrestris/metabolic_model/LRT1.sbml) respectively.

## Installation:
Install [PathwayTools](https://pathwaytools.com/) 29.0 as described on its homepage.
Clone this repository, go into the earthworm-models directory and install into your current Python environment with:

pip install .
