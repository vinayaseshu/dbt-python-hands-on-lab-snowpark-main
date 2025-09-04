## About the project
This repository is a code incomplete project that is used to create a fork in this [Snowflake quickstart](https://quickstarts.snowflake.com/guide/leverage_dbt_cloud_to_generate_ml_ready_pipelines_using_snowpark_python/index.html?index=..%2F..index#0). 

This repository showcases how to combine both SQL and python together in the same data pipeline to run both analytics and machine learning models on dbt Cloud. We are able to blend these together seamlessly using Snowpark for python on Snowflake.
The project utilizes open source Formula 1 data. This repository, dbt-snowflake-summit-2023-hands-on-lab-snowpark1, is code **incomplete and has dropped specific models** you build as part of the quickstart. 

As part of the quickstart you build insights for:
- Finding the lap time average and rolling average through the years
- Predicting the position of each driver based on a decade of data

First we fetch the Formula 1 data, hosted on a dbt Labs public S3 bucket. The code for this is under the `setup` folder in the file `setup_script_s3_to_snowflake.sql`. 
We will create a Snowflake Stage for our CSV files then use Snowflake's COPY INTO function to copy the data in from our CSV files into tables. The Formula 1 is available on Kaggle. The data is originally compiled from the Ergast Developer API. 
We will not be building the full pipeline as part of this workshop. Instead we will leverage an exisitng repo, fork it, and focus on our machine learning pipeline.

## Step by step quickstart
You can follow along how to build out some of the pipeline's code by following the [snowflake quickstart Leverage dbt Cloud to Generate ML ready pipelines using snowpark python](https://quickstarts.snowflake.com/guide/leverage_dbt_cloud_to_generate_ml_ready_pipelines_using_snowpark_python/index.html?index=..%2F..index#0).
The quickstart is abridged for time, meaning not every file in this repo is built from scratch. The quickstart utilizes this forked repository that has models (.sql and .py files) dropped from the [code complete repository](https://github.com/dbt-labs/python-snowpark-formula1) (called python-snowpark-formula1).

## Getting started
You do not need to create any local setup to replicate and run this project! 

All you need to get started are:
1. A Snowflake account with ACCOUNTADMIN access (you can spin up a trial account)
2. A GitHub Account

A dbt cloud account will be setup through a process called Partner Connect. This creates a dbt environment to login to, in browswer, that interpolates dbt code!

If you'd like to run this project locally, no problem! That setup won't be covered here and you should be familiar with using dbt core and Snowflake notebook connections locally. 

## What you can learn by exploring this repo:
- How to use dbt with Snowflake to build scalable transformations using SQL and Python
- How to use dbt SQL to prepare your data from sources to encoding
- How to train a model in dbt python and use it for future prediction

## Prerequisites 
To get the most out this repo it's best to have:
- Basic to intermediate SQL and python.
- Basic understanding of dbt fundamentals. We recommend the [dbt Fundamentals course](https://courses.getdbt.com/courses/fundamentals) if you're interested.
-  High level understanding of machine learning processes (encoding, training, testing)
- Simple ML algorithms — we will use logistic regression to keep the focus on the workflow, not algorithms!

**Bonus:** if you have completed the dbt workshop, [Accelerating Data Teams with Snowflake and dbt Cloud Hands On Lab](https://quickstarts.snowflake.com/guide/accelerating_data_teams_with_snowflake_and_dbt_cloud_hands_on_lab/index.html?index=..%2F..index#0), to have hands on keyboard practice with concepts like the source, ref, tests, and docs in dbt. 
By having completed that workshop, you will gain the most of this dbt python + snowpark workshop.

## Roadmap and future improvements
We will be updating this project from time to time for code cleanup, automation, and developing best practices.
So far the list of future improvements is as follows:
[ ] label encorder clean up for numeric variables <br>
[ ] ohe for the categorical variables <br>
[ ] multi-class accuracy <br>
[ ] saving accurary to a separate file to monitor model degradation/decay <br> 
[ ] trying out https://github.com/omnata-labs/dbt-ml-preprocessing for some of preprocessing?

## Contributing
If you want to contribute head over the [code complete repositiory](https://github.com/dbt-labs/python-snowpark-formula1) to suggest the changes there! 
Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated!! 
Really, any changes you'd like to see made to this project come to life is awesome!

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!

To make a contribution follow these steps:
1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/AmazingFeature)
3. Commit your Changes (git commit -m 'Add some AmazingFeature')
4. Push to the Branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

## Contact
Hope Watson &mdash; [LinkedIn](https://www.linkedin.com/in/hopewatson/)
[dbt slack community](https://www.getdbt.com/community/)

## Acknowledgments

I want to give a massive thanks to [Eda Johnson](https://www.linkedin.com/in/eda-johnson-saa-csa-pmp-0a2783/) at Snowflake. She was immensely helpful and in the python models you can see where her proof of concept served as the workflow we iterated on in this project.

Thanks to dbt Labs and my former manager and colleague, [Amy Chen](https://www.linkedin.com/in/yuanamychen/), for giving me the time to continue building skills and becoming technically more competent each day.
