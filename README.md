Welcome to your new dbt project!

### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [chat](https://community.getdbt.com/) on Slack for live discussions and support
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices


### Setup project in local:

### create a dbt project by the command: `dbt init <your_app_name>`


1. Create an enviroment in python 3+ version: virtualenv -p python3 env
2. Install the requirements: pip install -r requirement.txt
3. set configs in dbt_project.yml file:
    - name: '<your_app_name>'
    - models:
        dbt_app into --> 

    - models:
        <your_app_name>
    - profile: '<your_app_name>'
    
4. Now set up profiles.yml.
Note:
- When you invoke(`dbt run`) dbt from the CLI, dbt parses your dbt_project.yml for the name of the `profile` uses to connect to your data      warehouse.
- dbt then checks your `profiles.yml` file for a `profile`(in dbt_project.yml) with the same name.
- A profile contains all the details required to connect to your data warehouse.
- This file(`profiles.yml`) generally lives outside of your dbt project to avoid sensitive credentials being check in to version control.
- By default, dbt expects the profiles.yml file to be located in the ~/.dbt/ directory.

5. Copy profiles.yml.example file into another `profiles.yml` file which must exists here: ~/.dbt/.(if not exists create it manually.)

6. run `dbt debug` if all ok message should be: All checks passed

<!-- 6. change some configs like type, host, user, password.. -->

7. run `dbt seed` 

8. then `dbt run`.


Now can see tables and views created in your data warehouse.