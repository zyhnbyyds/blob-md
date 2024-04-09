### 你好吗， 哎呦


```js
async function handleDelete(rowData: ArticleItem) {
  await useFetch('/api/article/del', {
    method: 'DELETE',
    params: { id: rowData.id },
  })
  refresh()
}
```

### 你还能干嘛

啊啊