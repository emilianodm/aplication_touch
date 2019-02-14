# aplication_touch
prueba de touchstone

CREATE TABLE Players_info (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
firstname VARCHAR(30) NOT NULL,
lastname VARCHAR(30) NOT NULL,
email VARCHAR(50),
password char(64) not null,
reg_date TIMESTAMP
);

CREATE TABLE Players_stats (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
player_id int(6) NOT NULL,
player_tp VARCHAR(30) NOT NULL,
s_def int(3) NOT NULL,
s_reg int(3) NOT NULL,
s_pas int(3) NOT NULL,
s_vel int(3) NOT NULL,
s_fue int(3) NOT NULL,
reg_date TIMESTAMP
);

INSERT INTO `players_stats` (`id`, `player_id`, `player_tp`, `s_def`, `s_reg`, `s_pas`, `s_vel`, `s_fue`, `reg_date`) VALUES (NULL, '1', 'OFE', '83', '43', '84', '41', '50', CURRENT_TIMESTAMP);

select 
player_id, player_tp, avg(s_def) as s_def, avg(s_reg) as s_reg, avg(s_pas) as s_pas, avg(s_vel) as s_vel, avg(s_fue) as s_fue 
from players_stats;
