 ---Primo esercizio---
SELECT * FROM clienti
WHERE nome = 'mario';
---secondo esercizio---
SELECT nome, cognome FROM clienti
WHERE anno_di_nascita = 1960;
---terzo esercizio---
SELECT COUNT(*) AS numero_fatture
FROM fatture
WHERE iva = 20;
---quarto esercizio---
SELECT *
FROM prodotti
WHERE EXTRACT(YEAR FROM data_attivazione) = 2023
AND (in_produzione = TRUE OR in_commercio = TRUE);
---quinto esercizio---
SELECT f.numero_fattura, f.importo, c.nome, c.cognome, c.anno_di_nascita, c.regione_residenza
FROM fatture f
JOIN clienti c ON f.id_cliente = c.numero_cliente
WHERE f.importo < 1000;



