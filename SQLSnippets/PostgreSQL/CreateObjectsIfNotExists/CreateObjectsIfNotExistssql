CREATE TABLE IF NOT EXISTS customer (
	id		integer,
	name		varchar(100)
);

DO $$ 
    BEGIN
        BEGIN
            ALTER TABLE customer ADD COLUMN age int;
        EXCEPTION
            WHEN duplicate_column THEN RAISE NOTICE 'age column already exists.';
	END;
    END;
$$