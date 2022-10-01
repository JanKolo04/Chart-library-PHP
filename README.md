# Chart-library-PHP
Library with chart with people which visit webiste

## Requirements
### Tables
On start you nedd have to create two tables, first is `Move` to save moves on webiste and last 'Users'. You can copy code from down below. Id_user column are connect, because you can find fastest user which visit many times your website. In Date column in Move table you will saveing date when user visited website. 

```sql
//users table
CREATE TABLE `Users` (
  `id_user` int(255) NOT NULL,
  `Name` varchar(255) DEFAULT NULL,
  `Surname` varchar(255) DEFAULT NULL,
  `Email` text DEFAULT NULL,
  `Birth_date` date DEFAULT NULL
);

//move table
CREATE TABLE `Move` (
  `id_move` int(255) NOT NULL,
  `id_user` int(255) NOT NULL,
  'Count_visit' int(255) NOT NULL,
  `Date` date DEFAULT NULL,
  FOREIGN KEY (id_user) REFERENCES Users(id_user)
);
```

## Description
