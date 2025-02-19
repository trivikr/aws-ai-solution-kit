AI Solution Kit提供一系列基于深度学习的云上机器学习功能，例如文字识别、自然语言理解、人脸检测、图像理解等。您可以通过调用API，轻松使用开箱即用的AI功能，同时与亚马逊云科技提供的其它服务无缝集成。

## API列表

本方案通过Amazon API Gateway自动创建REST API，您在[部署解决方案](./deployment.md)后即可调用所需的AI功能。

下表列出了支持的API，您可以点击详情链接查看API接口的测试方法和示例代码。更多信息可参见[API参考指南](api-explorer.md)。

### 文字识别

| 名称            | 描述                                                                | API                                     |
|---------------|-------------------------------------------------------------------|-----------------------------------------|
| 轻量级文字识别（简体中文） | 通用场景文字提取，通过返回在图片中文字内容与坐标位置等信息，便于客户进行比对或结构化操作。支持识别简体中文、英文、数字和常用符号。 | [详情](deploy-general-ocr.md)             |
| 轻量级文字识别（繁体中文）  | 通用场景文字提取，通过返回图片中文字内容与坐标位置等信息，便于客户进行比对或结构化操作。支持识别繁体中文、英文、数字和常用符号。  | [详情](deploy-general-ocr-traditional.md) |
| 高阶文字识别（多语种）   | 识别并提取简体/繁体中文、越南文、日文、韩文、英文、数字、字母字符和符号。返回文本或坐标等相关信息。                | [Details](deploy-advanced-ocr.md)       |
| 自定义模板文字识别     | 客户可自定义OCR模板，提取卡证票据中结构化文字信息，并以键值对应关系的形式展现结果。                       | [详情](deploy-custom-ocr.md)              |
| 车牌信息识别        | 检测中华人民共和国境内常见机动车号牌，并识别其中的车牌号。                                     | [详情](deploy-car-license-plate.md)       |

### 人脸与人体

| 名称      | 描述                                                    | API                                         |
|---------|-------------------------------------------------------|---------------------------------------------|
| 人脸检测    | 识别人脸面部特征，将检测到的五官与轮廓关键点信息映射到64个矢量坐标上。                  | [详情](deploy-face-detection.md)              |
| 人脸相似度比对 | 通过两张人脸图片中的特征向量计算余弦相似度作为置信度，根据置信度比较，从而判断是否为同一个人。       | [详情](deploy-face-comparison.md)             |
| 人体结构化属性 | 识别输入图片中的人体区域，并返回每个区域人体位置坐标及属性分析，如性别、年龄、服饰等16种属性的语义信息。 | [详情](deploy-human-attribute-recognition.md) |
| 智能人像分割  | 基于AI深度学习框架识别图像中的人体轮廓，实现高精度分割，使之与背景进行分离。               | [详情](deploy-human-image-segmentation.md)    |

### 图像理解

| **名称** | **描述**                                                        |                                       |
|--------|---------------------------------------------------------------|---------------------------------------|
| 图像相似度  | 比较两幅图片是否相似，通过图片特征向量计算余弦距离，并转化为置信度，根据置信度比较两张图片的相似性。            | [详情](deploy-image-similarity.md)      |
| 通用物体识别 | 检测图像中的通用对象主体，返回该对象主体的区域信息与置信度。支持识别300类物体，详情可参见本文中支持的目标识别实体列表。 | [详情](deploy-object-recognition.md)    |
| 色情内容检测 | 自动对图片进行审核，获取多维度色情量化信息，如：normal，sexy，porn，实现精准快速的色情倾向判断。       | [详情](deploy-pornography-detection.md) |

### 视觉内容生产

| **名称** | **描述**                          |                                        |
|--------|---------------------------------|----------------------------------------|
| 图像超分辨率 | 可将图片智能放大2或4倍，从而获取清晰度更高、细节丰富的图像。同时支持图像修复。 | [详情](deploy-image-super-resolution.md) |

### 自然语言理解

| **名称**   | **描述**                                          |                                 |
|----------|-------------------------------------------------|---------------------------------|
| 文本相似度    | 比较两段不同文本之间相似度，并输出一个介于0到1之间的置信度，根据置信度比较两段文字的相似性。 | [详情](deploy-text-similarity.md) |
| 通用自然语言理解 | 提供多种中文文本理解类任务，如文本分类、情感分析、抽取，自定义标签体系等。           | [详情](deploy-general-nlu.md)     |

本实施指南介绍在Amazon Web
Services（亚马逊云科技）云中部署解决方案的架构信息和具体配置步骤。它包含指向CloudFormation模板的链接，这些模板使用亚马逊云科技在安全性和可用性方面的最佳实践来启动和配置本解决方案所需的亚马逊云科技服务。

本指南面向具有亚马逊云科技架构实践经验的IT架构师、开发人员、运维人员等专业人士。

<!--
### **语音技术**
|    **名称**   | **描述**    | **部署说明** |
|--------------|------------|-------------|
|||
-->