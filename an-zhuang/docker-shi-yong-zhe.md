# docker使用者

## 安装tracker

```bash
docker run 
    -tid 
    --name tracker 
    -v ~/tracker_data:/fastdfs/tracker/data 
    --net=host 
    season/fastdfs 
    tracker
```

## 安装storage

```
docker run 
    -tid
    --name storage 
    -v ~/storage_data:/fastdfs/storage/data 
    -v ~/store_path:/fastdfs/store_path 
    --net=host 
    -e TRACKER_SERVER:192.168.1.2:22122 
    season/fastdfs 
    storage
```



