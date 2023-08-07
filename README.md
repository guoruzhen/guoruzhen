- 👋 Hi, I’m @guoruzhen
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
guoruzhen/guoruzhen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
: # Build Stage
# 使用 golang:alpine 作为构建阶段的基础镜像
FROM golang:alpine AS builder

# 添加 git，以便之后能从GitHub克隆项目
RUN apk --no-cache add git

# 从 GitHub 克隆 go-proxy-bingai 项目到 /workspace/app 目录下
RUN git clone https://github.com/Harry-zklcdc/go-proxy-bingai.git /workspace/app
