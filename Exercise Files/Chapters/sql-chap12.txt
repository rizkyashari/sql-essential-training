-- 02 defined functions
-- album.db

SELECT SEC_TO_TIME(320);
SELECT TIME_TO_SEC('5:20');
SELECT title, duration, SEC_TO_TIME(duration) FROM track;

SELECT a.title, SUM(duration), SUM_SEC_TO_TIME(t.duration) FROM track AS t
  JOIN album AS a ON t.album_id = a.id
  GROUP BY a.id
