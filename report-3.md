# Lab Report #3
## `grep` Command
* `grep -c`
   <ol>
      <li>This command returns the count of the amount of times a given word(s) appears in a file. In both the situations below, we look at the WhereToMadrid.txt 
          to find how many times the words "museums", "sculptures", "Italian", and "Spanish" are used. This is useful as it could help determine whether a 
          certain string's repetitions increase or not. </li>
   </ol>
   
   My source: [https://phoenixnap.com/kb/grep-multiple-strings](url) 
```
grep -c 'museums\|sculptures' written_2/travel_guides/berlitz1/WhereToMadrid.txt
11
```
```
grep -c 'Italian\|Spanish' written_2/travel_guides/berlitz1/WhereToMadrid.txt
31
```
* `grep -R`
     <ol>
      <li>This command reads all files under a given directory and returns matches of the strings passed into the command. Each line of output will contain the file
          along with the phrase/sentences the string is found in. This is useful for when we want to search an entire directory for a given string, without this command
          it would be much more work testing each file individually. </li>
   </ol>
   
   My source:[https://phoenixnap.com/kb/grep-multiple-strings](url)
   ```
   grep -R 'museums\|sculptures' written_2/travel_guides/berlitz1/*.txt
   written_2/travel_guides/berlitz1/HistoryFrance.txt:        cinema, museums, and libraries, and also for scientific research.
   written_2/travel_guides/berlitz1/HistoryGreek.txt:        original examples in the archaeological museums throughout the
   written_2/travel_guides/berlitz1/HistoryIbiza.txt:        archaeological museums.
   written_2/travel_guides/berlitz1/HistoryIndia.txt:        bronze and stone sculptures of Buddha.
   written_2/travel_guides/berlitz1/HistoryIndia.txt:        engineers, and huge sculptures were ordered from Victorian Britain
   ```
   ```
   grep -R 'Italian\|Spanish' written_2/travel_guides/berlitz1/
   written_2/travel_guides/berlitz1//HistoryJapan.txt:        like the Portuguese and Spanish Catholic missionaries, who he felt were
   written_2/travel_guides/berlitz1//HistoryJamaica.txt:        found at their settlements near Nueva Sevilla and Spanish Town have
   written_2/travel_guides/berlitz1//HistoryJamaica.txt:        been identified, and it is said that when the Spanish arrived in
   written_2/travel_guides/berlitz1//HistoryJamaica.txt:        the island. The Spanish immediately began subjugating the Arawak
   written_2/travel_guides/berlitz1//HistoryJamaica.txt:        rather than live the life created for them by the Spanish.
   ```
   
* `grep -w` 
    <ol>
      <li>This command prints out each sentence where the strings passed in are found within the file. It gives back exact matches, which is
      useful for when we want to keyword search a file rather than read through the whole thing. 
  </li>
  </ol>
  
  My source: [https://phoenixnap.com/kb/grep-multiple-strings](url)
  
  ```
  grep -w 'museums\|sculptures' written_2/travel_guides/berlitz1/WhereToMadrid.txt
  Barrio de Salamanca is the most attractive
        gardens, and museums. Less than 2 km (about a mile) from the royal
        Aside from the palaces and museums, Aranjuez is noted for
        flowers, clipped hedges, sculptures, and fountains.
  ```
  ```
  grep -w 'Italian\|Spanish' written_2/travel_guides/berlitz1/WhereToMadrid.txt
  Even apart from its Spanish treasures, it
        famous foreign works, especially of the Italian and Flemish schools.
        renovation and work on an extension are underway.
  ```
  
* `grep -i`
   <ol>
     <li>This command prints out each sentence where the strings passed in are found within the file while ignoring case. It returns the sentences that use the strings passed in, which 
      makes keyword searching more efficient as the user is given all the times that word is used without having to search multiple times with different case scenarios.
   </li>
   </ol>
    
   My source: [https://phoenixnap.com/kb/grep-multiple-strings](url)
   ```
   grep -i 'Museums\|Sculptures' written_2/travel_guides/berlitz1/WhereToMadrid.txt
   Seeing and
        banks and smaller museums. Barrio de Salamanca is the most attractive
        gardens, and museums. Less than 2 km (about a mile) from the royal
        Aside from the palaces and museums, Aranjuez is noted for
        flowers, clipped hedges, sculptures, and fountains.
   ```
   ```
   grep -i 'Italian\|spanish' written_2/travel_guides/berlitz1/WhereToMadrid.txt
       the Spanish call El Bosco, has three masterpieces in the Prado,
        Italian: Titian (c. 1490–1576) is represented by several
        your way through the Italian rooms, be sure to keep an eye peeled for
        houses the Centro de Arte Reina Sofía. 
   ```
