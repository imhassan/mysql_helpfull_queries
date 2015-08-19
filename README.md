## Change DB Engine from MyISAM to InnoDB.
``
SELECT CONCAT(  'ALTER TABLE ', table_schema,  '.', table_name,  ' engine=InnoDB;' )
FROM information_schema.tables
WHERE ENGINE =  'MyISAM'
AND table_schema =  'DB-NAME'
``
