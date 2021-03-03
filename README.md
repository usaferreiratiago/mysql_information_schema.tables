# mysql_information_schema.tables

SELECT  
TABLE_CATALOG,
CONCAT('SELECT * FROM',' ',TABLE_SCHEMA,'.',
lower(TABLE_NAME),';') AS 'INFORMATION SCHEMA',
TABLE_TYPE,
ENGINE,
VERSION,
TABLE_ROWS,
AUTO_INCREMENT,
CREATE_TIME,
UPDATE_TIME,
CHECK_TIME,
TABLE_COLLATION,
TABLE_COMMENT
FROM information_schema.tables
where table_schema = 'information_schema';
