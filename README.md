# revpage

##Paginator for Revel

Thanks for beego!
The code copied from beego pagination, modified for revel.Request.

##Usage
In revel controller
```
record := new(models.Adapter)
t_count, _ := record.Count(query, c.MongoSession)
count := int64(t_count)
paginator := revpage.NewPaginator(c.Request, perPage, count)
//Query data
results, err := record.SearchByPage(query, perPage, paginator.Offset(), c.MongoSession)

return c.Render(records, paginator)

```
In template

refer to paginator.html
