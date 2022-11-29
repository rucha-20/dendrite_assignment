### database
--user
create table users(
    user_id integer primary key auto_increment,
    firstName varchar(50) not null,
    lastName varchar(50) not null,
    email varchar(50) not null,
    pw varchar(100) not null,
    age integer,
    gender varchar(5)
);

insert into user (firstName,lastName,email,pw,age,gender) values ("Rucha","Inamdar","rucha18inamdar@gmail.com","abc",25,"F");
insert into user (firstName,lastName,email,pw,age,gender) values ("Radhika","Joshi","radhika@gmail.com","wec",25,"F");
insert into user (firstName,lastName,email,pw,age,gender) values ("Rajat","Joshi","rajat@gmail.com","wer",25,"M");

--songs
create table songs(song_id integer primary key auto_increment,
song_name varchar(50) not null,
song_composer varchar(50) not null,
song_genre1 varchar(50) not null);

insert into songs(song_name,song_composer,song_genre) values("Mitwa","Shankar Ehsan Loy","Romantic");
insert into songs(song_name,song_composer,song_genre) values("Channa Mereya","Pritam","Sad");
insert into songs(song_name,song_composer,song_genre) values("Aashayein","Salim Sulaiman","Motivational");

--favorites
create table favorites(song_name varchar(50) not null, 
user_id integer,
foreign key(user_id) references user(user_id));