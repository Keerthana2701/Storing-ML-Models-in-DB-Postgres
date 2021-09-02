# Storing and Retrieving-ML-Models-in-DB using Postgres
-- To create a table. type the below in notepad with model id,name and file and save with .sql :

create schema modelstore;

DROP TABLE IF EXISTS modelstore.futurex_model_catalog;
CREATE TABLE modelstore.futurex_model_catalog
(
    model_id integer NOT NULL,
    model_name character varying COLLATE pg_catalog."default" NOT NULL,
    model_file bytea NOT NULL
);


-- pass the values as tuple with id, name nad file ==== (2, 'sc', pickle_sc_string)
-- store pickle strings into postgres table here id,name, pickled binary string

-- cursor is used to execute the query

-- model is saved in DB. any application can access this model from this table and do prediciton
