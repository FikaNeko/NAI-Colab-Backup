# 在您使用之前请阅读README！
## 使用方法
点击该仓库的Code，点击Download ZIP下载解压包然后解压，打开Google Colab https://colab.research.google.com/ 登录自己的Google账号后点击左上角文件，点击上传笔记本，这里有两个使用不同的前端的版本，“NovelAILeaks_API_Backend_(4chan_Ver_)”.ipynb为NovelAI官方前端，StableDiffusionUI_(adapted_to_NovelAILeaks).ipynb为Stable Diffusion前端
## NovelAI前端与Stable Diffusion前端对比
### NovelAI前端优缺点
优点：不需要过多配置，直接输入Prompt即开即用，生成效果比使用Stable Diffusion前端的更好一点（未知原因，个人猜测Stable Diffusion前端和NovelAI前端使用了不同的模型，NovelAI使用animefull-final-lastest模型，Stable Diffusion使用animefull-final-pruned模型）
缺点：生成多张图后端会卡图出现错误，不能生成图片（未知原因），这种情况下需要刷新前端页面重新填入Prompt，建议一次生成的图片不要超过2张
### Stable Diffusion前端优缺点
优点：可玩性较高，可自由调节各种参数，有txt2img、img2img和inpaint等实用功能，生成效果也不错，一次可以生成很多张图，不会卡图
缺点：在您第一次开始前需要做一些设置保证出图质量，操作较为繁琐
## 针对Stable Diffusion前端的一些设置
### 基础设置
转到Settings划到底下将Stop At last layers of CLIP model的数值设置为2，然后Apply Settings，在Negative Prompt输入负面Prompt，这里有一串针对单人生成图片的负面Prompt：

{Multiple people},lowres,bad anatomy,bad hands, text, error, missing fingers,extra digit, fewer digits, cropped, worstquality, low quality, normal quality,jpegartifacts,signature, watermark, username,blurry,bad feet,cropped,poorly drawn hands,poorly drawn face,mutation,deformed,worst quality,low quality,normal quality,jpeg artifacts,signature,watermark,extra fingers,fewer digits,extra limbs,extra arms,extra legs,malformed limbs,fused fingers,too many fingers,long neck,cross-eyed,mutated hands,polar lowres,bad body,bad proportions,gross proportions,text,error,missing fingers,missing arms,missing legs,extra digit

然后将Sampling Steps设置为40（建议），Sampling Steps为生成图片的迭代步数，步数越高不代表生成的图片越好，但步数低了肯定不会生成好图，建议步数不要低于28，生成竖向图将Height设置为768，生成横向图将Width设置为768，将CFG Scale设置为12（建议），Batch count为生成图数量，可自行设置
### 进阶设置
#### 关于img2img的设置
Denoising Strength 指与原图的差异度，建议在 0.75-0.9，魔改图片可以设为 0.5 以下，数值越小，与原图的相似度越高，CFG Scale描述的是生成的图片与文字描述的拟合度，可以根据Prompt和期望图片自行调整，建议设置为7~18
如果想要了解更多进阶使用方法请点击这里：https://zhuanlan.zhihu.com/p/570954565
您可以在这里查询各种tags: https://aitag.top/