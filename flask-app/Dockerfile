# 使用from关键字制定基本镜像
FROM alpine:3.6

# 编写复制文件和安装依赖关系的命令
RUN apk add --update py2-pip

# 安装Python应用程序所需的Python模块
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

# 复制应用程序运行所需的文件
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

# 告诉容器应该暴露的端口号
EXPOSE 5000

# 运行app
CMD ["python", "/usr/src/app/app.py"]
