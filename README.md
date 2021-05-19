# Attachments
Attachments
%load_ext autoreload
%autoreload 2
import warnings

warnings.simplefilter("ignore")
from pathlib import Path

import geopandas as gpd
import numpy as np
import pandas as pd
from powergenome.generators import GeneratorClusters
from powergenome.GenX import reduce_time_domain
from powergenome.load_profiles import make_final_load_curves
from powergenome.params import DATA_PATHS
from powergenome.util import (
    build_scenario_settings,
    init_pudl_connection,
    load_settings,
)
from powergenome.external_data import (
    make_demand_response_profiles,
    make_generator_variability,
)

pd.options.display.max_columns = 200
