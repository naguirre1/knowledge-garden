---
type: daily
description: A basic structure for a daily note that evolves over the day
tags:
  - daily-note
  - todo-list
related: "[[⏰ ToDo Lists]]"
---
%%
Status:: #in-progress
%%

---

# 1. Goals
### xx
### xx

---
# 2. Daily


**wkleiruyfvb** *dijkbc* 

`codigo`

``` Javascript
{
OBJETO.metodo.hc;wiejbc: 
}
```

# 3. Doing
# 4. Questions
# 5. Pending tasks

``` dataview 
TASK FROM #todo-list WHERE !completed AND !checked AND file.name != "🪛 Todo List" GROUP BY file.link SORT file.mtime DESC 
```


----

# New Items Created

```dataview
table file.ctime as "Planted at",
file.mtime as "Last tended to",
length(file.inlinks) as "In Links", 
length(file.outlinks) as "Out Links"
where date(file.cday) <= (date(this.file.cday) + dur(1 day))
and date(file.cday) >= date(this.file.cday)
and this.file.name != "🗓 Daily Note"
```
---

<!-- Put links to new items created here -->