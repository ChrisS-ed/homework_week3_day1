Week 3, Day 1 homework

SECTION 1

***** Select the names of all users.
SELECT name FROM users;     
       name       
------------------
 Rick Henri
 Jay Chetty
 Keith Douglas
 Callum Dougan
 Andrew Insley
 Daniel Gillespie
 Bethany Fraser
 Nick Ridell
 Evelyn Utterson
 Sky Su
 Nicholas Hill
 Michael McLeod
 Callum Hogg
 Chris Sloan
 Gary Carmichael
 Oscar Brooks
 Ross Galloway
 Paul MacLean
 Stuart Ramsay
 Peter Forbes
 Euan Walls
 Aine Dunphy
 (22 rows)

***** Select the names of all shows that cost less than £15.
SELECT name FROM shows WHERE price < 15;
             name             
------------------------------
 Le Haggis
 Paul Dabek Mischief 
 Best of Burlesque
 Two become One
 Urinetown
 Two girls, one cup of comedy
(6 rows)

***** Insert a user with the name "Val Gibson" into the users table.
INSERT INTO "users" (name) VALUES ('Val Gibson');
INSERT 0 1
23 | Val Gibson

***** Select the id of the user with your name.
SELECT id FROM users WHERE name = 'Chris Sloan';
id 
----
 14
(1 row)

***** Insert a record that Val Gibson wants to attend the show "Two girls, one cup of comedy".
INSERT INTO "shows_users" (show_id, user_id) VALUES (12, 23);
INSERT 0 1
 id | show_id | user_id 
----+---------+---------
 82 |      12 |      23
(1 row)

***** Updates the name of the "Val Gibson" user to be "Valerie Gibson".
UPDATE users SET name = 'Valerie Gibson' WHERE name = 'Val Gibson';
UPDATE 1
23 | Valerie Gibson

***** Deletes the user with the name 'Valerie Gibson'.
DELETE FROM users WHERE name = 'Valerie Gibson';
DELETE 1

***** Deletes the shows for the user you just deleted.
DELETE FROM shows_users WHERE user_id = 23;
DELETE 2

