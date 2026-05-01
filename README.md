# ip-content-system
选题枯竭、脚本 / 文案创作耗时、多平台适配成本高、用户互动维护难
快速启动
方式一：Docker 一键部署（推荐）
bashcd K:\111\ip-content-system

# 1. 配置 LLM API Key
cp .env.example .env
# 编辑 .env，填入 LLM_API_KEY

# 2. 启动
docker compose up -d

# 3. 访问
# 前端: http://localhost
# API:  http://localhost:8000/docs
方式二：本地开发（需要 Python 3.12 + Node 20）
bash# 终端1：启动 PostgreSQL（需已安装），然后：
cd ip-content-system\backend
pip install -r requirements.txt
uvicorn app.main:app --reload

# 终端2：
cd ip-content-system\frontend
npm install
npm run dev
