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
paginator := pagination.NewPaginator(c.Request, perPage, count)
results, err := record.SearchByPage(query, perPage, paginator.Offset(), c.MongoSession)

```
In template

refer to paginator.html
