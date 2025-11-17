--------------------------------- README ---------------------------------------
1. buat database di postgresql
2. buat table beserta kolomnya.
   QUERY NYA
   -- Data Preparation

      CREATE TABLE public.layoffs_2(
          company              TEXT,
          location             TEXT,
          industry             TEXT,
          total_laid_off       INTEGER,
          percentage_laid_off  NUMERIC(10,2),
          layoff_date          TEXT,
          stage                TEXT,
          country              TEXT,
          funds_raised         NUMERIC(12,2)
      );
      
      SELECT * FROM layoffs_2;


   
3. import file dataset csv nya.
   untuk import file bisa ikuti promt berikut
   
       \copy public.layoffs_2
       FROM 'C:\Users\yuliatun\Documents\DATA ANALIS\SQL\layoffs.csv'
       WITH (
         FORMAT csv,
         DELIMITER ',',
         HEADER,
         QUOTE '"',
         NULL 'NULL'
       );
5. lalu bisa copy file layoff.sql
