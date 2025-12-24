---
created: <% tp.file.creation_date() %>
tags:
  - "#Daily"
---


# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>

<< [[Timestamps/<% tp.date.now("YYYY", -1) %>/<% tp.date.now("MM-MMMM", -1) %>/<% tp.date.now("YYYY-MM-DD-dddd", -1) %>|Yesterday]] | [[Timestamps/<% tp.date.now("YYYY", 1) %>/<% tp.date.now("MM-MMMM", 1) %>/<% tp.date.now("YYYY-MM-DD-dddd", 1) %>|Tomorrow]] >>

---
# Daily Questions
## One thing I'm excited about right now is...
- 

## One+ thing I plan to accomplish today is...
- [ ] 

## One+ thing I didn‘t accomplish before is...
```dataview
TASK
WHERE !completed and created < date(today)
```

## One thing I'm struggling with today is...
- 

---
# Notion
- <% tp.file.cursor() %>

---
### Notes created today
```dataview
List
FROM "" 
WHERE file.cday = date(today) 
SORT file.ctime asc
```

### Notes last touched today
```dataview
List 
FROM "" 
WHERE file.mday = date(today) 
SORT file.mtime asc
```
