# RUIFLOW Studio v1.0
## 全风格3D骨骼驱动AI动漫视频生成平台

---

## 🎯 v1 核心功能
1. **3D骨骼解析**: 支持GLB/GLTF格式3D文件自动解析为OpenPose骨骼图
2. **4种内置风格**: 武侠国风/日系动漫/美系英雄/科幻未来
3. **三道防线自动质检**: 不合格自动重生成，保证出品质量
4. **一键启动**: 双击启动脚本，开箱即用

---

## 📦 交付物清单

| 文件 | 说明 |
|------|------|
| `glb_to_openpose.py` | 3D骨骼→OpenPose转换脚本 |
| `comfy_api.py` | ComfyUI API调用封装 |
| `quality_check.py` | 三道防线自动质检脚本 |
| `app.html` | 极简前端界面 |
| `start_ruiflow.sh` | 一键启动脚本 |
| `output/poses/default_standing_openpose.png` | 内置默认站立姿势骨骼图 |
| `ComfyUI/verify_8frame.json` | 8帧动画工作流 |
| `ComfyUI/verify_single_frame.json` | 单帧生成工作流 |

---

## 🚀 快速启动

### 1. 启动ComfyUI（如果没启动）
```bash
cd /Users/liuxiansheng/Documents/comfy/ComfyUI
python3 main.py --listen 0.0.0.0 --port 8188
```

### 2. 启动RUIFLOW
```bash
cd /Users/liuxiansheng/.openclaw/workspace-main
./start_ruiflow.sh
```

### 3. 访问界面
打开浏览器访问: `http://localhost:3000/app.html`

---

## 📖 使用说明

1. **上传3D文件**: 点击上传GLB/GLTF格式骨骼动画文件
2. **选择风格**: 4种风格任选
3. **点击生成**: 等待生成完成，自动质检，不合格自动重试
4. **下载结果**: 生成完成后点击下载MP4

---

## 🏛️ 三道质量防线

| 防线 | 检查内容 |
|------|---------|
| 防线1 | 基础完整性：文件大小、分辨率、帧数 |
| 防线2 | 视觉质量：亮度、对比度、模糊度 |
| 防线3 | 人物完整性：肤色占比、面部检测 |

---

## 🔧 技术栈
- 基础模型: Stable Diffusion 1.5
- 视频生成: AnimateDiff v3
- 骨骼控制: ControlNet OpenPose
- 前端: 纯HTML/JS，无框架
- 后端: ComfyUI + Python

---

## 📅 v2 规划
1. 更多3D格式支持（FBX, BVH）
2. 人物一致性保持
3. 可插拔资产系统
4. 三大编辑窗口：人物/动作/场景
5. 云端部署

