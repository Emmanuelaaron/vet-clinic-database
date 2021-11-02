# SELECT COUNT(*) FROM visits where animal_id = 4;

For the first part we verify the tables and realize that there was no need to modify any of the tables, but we agree that the problem was on the data query itself, so we modify the request to be: 
```
SELECT COUNT(animal_id) FROM visits where animal_id = 4;
```
So the query only takes in cosideration the animal_id colum. 

When we test it out we realize that the execution time was reduce from 1751ms to just 829ms.


# SELECT * FROM visits where vet_id = 2;

For this part we created an index for the column vet_id using:
   ```CREATE INDEX visits_vet_id_asc ON visits(vet_id ASC);```

When we tested it we realized that the execution time reduced from 3995.222 ms to 3621.804 ms