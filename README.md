# Data and code for Arkansas individual and business tax reform analysis
This repository contains the data and code for the analyses by [Richard W. Evans](https://sites.google.com/site/rickecon) (@rickecon) in the November 2024 article on Arkansas individual and business tax reform.

## How to run the code from these analyses in the cloud in your browser
We have created a [Google Colab notebook](https://colab.research.google.com/drive/1MLDJtMhEMF11oFazq3-JlHRYWhynOIqg?usp=sharing) with code almost exactly the same as th code in the Jupyter Notebook [`AR_IndivBusTax.ipynb`](AR_IndivBusTax.ipynb) decribed in the next section. The [Google Colab notebook](https://colab.research.google.com/drive/1MLDJtMhEMF11oFazq3-JlHRYWhynOIqg?usp=sharing) has the advantage of using a distribution of Python and corresponding packages that run in the cloud on remote servers instead of on your local machine. This allows you to use the notebook from any kind of device with a browser. You can execute th code, see the results, and save output to a temporary cloud folder from which you can download anything you want to keep.

## How to run the Jupyter Notebook on your machine
This repository contains a Jupyter Notebook [`AR_IndivBusTax.ipynb`](AR_IndivBusTax.ipynb) that can be run locally on your own machine to replicate the analyses in the paper. You can also modify this notebook to use for other analyses you might want to experiment with. To run this notebook locally on your machine, do the following steps:
* Fork and clone (or download) the https://github.com/OpenSourceEcon/AR-IndivBusTax repository
* In your computer's terminal, navigate to the directory of the `AR-IndivBusTax` repository on your local machine.
* Create the conda environment `ar-indivbustax-dev` by typing the following command: `conda env create -f environment.yml`
* Activate the `ar-indivbustax-dev` conda environment by typing the following command: `conda activate ar-indivbustax-dev`
* This should allow your notebook to run while this conda environment is activated.

## Files and directories in the repository
This repository contains the following items:
* [`AR_IndivBusTax.ipynb` Jupyter notebook](AR_IndivBusTax.ipynb). An executable notebook you can use to replicate all the analyses in the article and creation of output and figures. A corresponding [Google Colab notebook](https://colab.research.google.com/drive/1MLDJtMhEMF11oFazq3-JlHRYWhynOIqg?usp=sharing) that can be run on your browser and executed in the cloud is available at the link in this sentence.
* [`environment.yml`](environment.yml). Conda environment file for creating conda environment `ar-indivbustax-dev`.
* [`/data/` directory](data/). This directory contains the data used in the analyses in the article.
    * [`/data/21instateshares.csv`](/data/21instateshares.csv). IRS Statistics of Income State Tax Statistics from 2021. This data is used to in the cost estimate of the flat tax policy.
    * [`/data/cb_2018_us_state_20m`](/data/cb_2018_us_state_20m). Folder containing US Census Bureau shapefiles (7 files) and corresponding files for US states. We use the "<1.0 MB" files (the `_20m` extension). See https://www.census.gov/geographies/mapping-files/2018/geo/carto-boundary-file.html. These are used in the creation of the [`/images/fig1_state_taxtype_2024.html`](/images/fig1_state_taxtype_2024.html) and [`/images/fig2_state_corptaxtype_2024.html`](/images/fig2_state_corptaxtype_2024.html) map images in [`AR_IndivBusTax.ipynb` Jupyter notebook](AR_IndivBusTax.ipynb).
    * [`/data/fig1_state_taxtype_2024.csv`](/data/fig1_state_taxtype_2024.csv). Source data for Figure 1 in the paper.
    * [`/data/fig2_state_corptaxtype_2024.csv`](/data/fig2_state_corptaxtype_2024.csv). Source data for Figure 2 in the paper.
    * [`/data/fig4_source.csv`](/data/fig4_source.csv). Source data for Figure 4 in the paper.
    * [`/data/fig5_source.csv`](/data/fig5_source.csv). Source data for Figure 5 in the paper.
    * [`/data/fig8_source.csv`](/data/fig8_source.csv). Source data for Figure 8 in the paper.
    * [`/data/NST-EST2023-ALLDATA.csv`](/data/NST-EST2023-ALLDATA.csv). US Census Bureau net domestic migration by state data for 2023.
    * [`/data/Pew_ReservesData.csv`](/data/Pew_ReservesData.csv). Rainy Day Fund and Total Reserves and Balances data for all 50 states and DC, Pew Charitable Trusts, Sep. 19, 2024, accessed Sep. 24, 2024 (Data downloaded from: https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2014/fiscal-50/reserves-and-balances)
    * [`/data/tab3_netmigr_rank_full_2023.csv`](/data/tab3_netmigr_rank_full_2023.csv). Net migration data with all variables.
    * [`/data/Tab13comp.xlsx`](/data/Tab13comp.xlsx). Worksheets for computing cost estimates in Table 13.
* [`/images/` directory](images/). This folder contains the `.html` files for the dynamic visualizations in the paper and created in the notebook and the corresponding static `.png` image files.
    * [`/images/fig1_state_taxtype_2024.html`](/images/fig1_state_taxtype_2024.html). Dynamic data visualization Bokeh `.html` file. Figure 1. US State Employment Income Tax Systems as of July 2024.
    * [`/images/fig1_state_taxtype_2024.png`](/images/fig1_state_taxtype_2024.png). Static `.png` file. Figure 1. US State Employment Income Tax Systems as of July 2024.
    * [`/images/fig2_state_corptaxtype_2024.html`](/images/fig2_state_corptaxtype_2024.html). Dynamic data visualization Bokeh `.html` file. Figure 2. US State Corporate Income Tax Systems as of July 2024.
    * [`/images/fig2_state_corptaxtype_2024.png`](/images/fig2_state_corptaxtype_2024.png). Static `.png` file. Figure 2. US State Corporate Income Tax Systems as of July 2024.
    * [`/images/fig3_net_domestic_migration_2023.html`](/images/fig3_net_domestic_migration_2023.html). Dynamic data visualization Bokeh `.html` file. Figure 3. 2023 net domestic migration as percent of 2022 population.
    * [`/images/fig3_net_domestic_migration_2023.png`](/images/fig3_net_domestic_migration_2023.png). Static `.png` file. Figure 3. 2023 net domestic migration as percent of 2022 population.
    * [`/images/fig4_ar_raintotbal_tseries.html`](/images/fig4_ar_raintotbal_tseries.html). Dynamic data visualization Bokeh `.html` file. Figure 4. Arkansas Rainy Day fund and total reserves as a percentage of general fund expenditures: 2000-2024.
    * [`/images/fig4_ar_raintotbal_tseries.png`](/images/fig4_ar_raintotbal_tseries.png). Static `.png` file. Figure 4. Arkansas Rainy Day fund and total reserves as a percentage of general fund expenditures: 2000-2024.
    * [`/images/fig5_rain_totbal_pct_2024.html`](/images/fig5_rain_totbal_pct_2024.html). Dynamic data visualization Bokeh `.html` file, for web publication. Figure 5. State 2024 Rainy day Fund Balances and Total Fund Balances as Percent of General Fund Expenditures.
    * [`/images/fig5_rain_totbal_pct_2024.png`](/images/fig5_rain_totbal_pct_2024.png). Static `.png` file, for web publication. Figure 5. State 2024 Rainy day Fund Balances and Total Fund Balances as Percent of General Fund Expenditures.
    * [`/images/fig6_CurrReformTaxRates.html`](/images/fig6_CurrReformTaxRates.html). Dynamic data visualization Bokeh `.html` file, for web publication. Figure 6.
    * [`/images/fig6_CurrReformTaxRates.png`](/images/fig6_CurrReformTaxRates.png). Static `.png` file, for web publication. Figure 6.
    * [`/images/fig7_CurrReformAR_StdDeduct_3.html`](/images/fig7_CurrReformAR_StdDeduct_3.html). Dynamic data visualization Bokeh `.html` file, for web publication. Figure 7.
    * [`/images/fig7_CurrReformAR_StdDeduct_3.png`](/images/fig7_CurrReformAR_StdDeduct_3.png). Static `.png` file, for web publication. Figure 7.
    * [`/images/fig8_NetStateTaxLiabChg_3.html`](/images/fig8_NetStateTaxLiabChg_3.html). Dynamic data visualization Bokeh `.html` file, for web publication. Figure 8.
    * [`/images/fig8_NetStateTaxLiabChg_3.png`](/images/fig8_NetStateTaxLiabChg_3.png). Static `.png` file, for web publication. Figure 8.
    * [`/images/fig9_HistAR2024revenue.html`](/images/fig9_HistAR2024revenue.html). Dynamic data visualization Bokeh `.html` file, for web publication. Figure 9.
    * [`/images/fig9_HistAR2024revenue.png`](/images/fig9_HistAR2024revenue.png). Static `.png` file, for web publication. Figure 9.
