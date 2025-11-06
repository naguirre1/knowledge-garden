```dataview
TABLE WITHOUT ID
    file.link as "Término",
    description as "Definición breve"
FROM #term
WHERE type = "term"
GROUP BY substring(file.name, 0, 1)
SORT substring(file.name, 0, 1) ASC
```