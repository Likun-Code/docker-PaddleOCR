# docker-PaddleOCR

## 创建镜像
```
docker build --no-cache -t likun-code/ppocr .
```

## docker运行
```
docker run --name ppdocr -p 8866:8866 -d likun-code/ppocr`
```

## docker-compose运行
```
docker-compose up -d
```

## 发送请求
a. 计算待识别图片的Base64编码
b. 发送服务请求
```
curl -H "Content-Type:application/json" -X POST --data "{\"images\": [\"填入图片Base64编码(需要删除'data:image/jpg;base64,'）\"]}" http://localhost:8866/predict/ocr_system
```
