# 使用官方Python运行时作为父镜像
FROM python:3.8-slim-buster

# 设置工作目录
WORKDIR /app

# 将当前目录内容复制到容器的/app中
ADD . /app

RUN pip install --upgrade pip -i https://pypi.tuna.tsinghua.edu.cn/simple
# 安装程序需要的包
RUN pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

# 运行时监听的端口
EXPOSE 8002

# 设置默认运行参数
# SK_KEY 接口调用认证Token
# 设置 uvicorn 参数 workers 的数量
ENV SK_KEY sk-abcdefghijkabcdefghijkabcdefghijk
ENV NUM_WORKERS 1

# 运行容器时的命令及其参数
CMD ["python", "openai_api.py"]