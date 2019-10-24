# Data Engineer Applicant Exercise
To be considered for a Data Engineer position at **Overactive**, you must
successfully complete these steps.

## What is the exercise about?

Brief. 
You will:  
1. Download data from a public API to a dabase of your choice.
2. [OPTIONAL] Create your own API to read the data from your database.
3. Create a SQL report.
4. Automate your pipeline in the cloud.

## Detailed Tasks ##

1. First of all, fork this repository to your GitHub account and clone your own repo to your laptop.
  * If you are not familiar with GitHub, please check this
  [how to fork a repo](https://help.github.com/articles/fork-a-repo/) link.
2. To initialize the workspace, please create a folder named `working_folder`
or execute the following command. **IMPORTANT: All exercise deliverables should
be in this folder before submitting the application.**
```
make init
```
3. Once in your **initilized** repository, in the `working_folder` directory and using the
programming language/tool of your preference, create a script that collects the
`consolidated_weather` from the 3 different cities/regions of your election from
 [this](https://www.metaweather.com/api/) public API, and save it to a local file.
3. Again in your repository, in the `working_folder` directory and using the
programming language/tool of your preference, create a second script that uploads
previous CSV files to either a MongoDB or a PostgreSQL database.
  * You can use [mLab](https://mlab.com/plans/pricing/#plan-type=sandbox) to start
  a free MongoDB as a Service.
  * If you prefer a PostgreSQL database, you can use [ElephantSQL](https://www.elephantsql.com/plans.html)
  to start a free PostgreSQL server.
  * If you do not want to use any of these cloud providers you can use a SQLite database.
4. [OPTIONAL] Once you load the data into the DB you choose, create a directory inside the working folder and name it `app`.
Inside the folder build an API to consume the data you just load into the db. Choose the framework, 
or programming language you want there is no restriction. The API calls should have a persistence in a db.
5. In the `working_folder` create a directory call `querys` and create a text file called `query.txt` with the
query code to get a report of how accurate is `wind_speed` prediction with time.
  * Taking day X as a reference, which is the deviation from `wind_speed(X)` compared
 with previous predictions of the same day X.
6. Following the Serverless approach, put this pipeline to automatically
run on a daily basis.
  * You can use Heroku, AWS Free Tier or Google Cloud.
  * You can use the Serverless Framework and just make the yaml config for the deploy.
  * You can create a Dockerfile with the enviroment and just write in a txt how you will set up a cron job.
  * Add another document in the `working_folder` explaining how you did it and
  some evidences.
7. [OPTIONAL] Try yo load the CSV files downloaded from the api using an event processing platform. You can choose the 
   event platform you want Kafka, RabbitMQ, Celery... etc. There is not need to create the full architecture code, but
   otherwise create a file called streaming_events.txt explaining us how will you build this architecture.

** If you find any issues during the exercise, please send an email to [jobs@overactive.com](mailto:jobs@overactive.com)
