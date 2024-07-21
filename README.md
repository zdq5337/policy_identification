# 书生·浦语大模型实战营项目：保单OCR识别

## 项目背景
在保险行业，各类纸质单据的信息化录入主要还是依靠纯手工处理，对于保险保单这类多达数百种、信息量大且结构复杂的数据录入需求，更是行业的一大痛点。再者，由于技术、数据、成本上的高门槛，保单数据结构化处理类的技术和产品仍较为稀缺。本项目旨在将不同寿险保司的保单中的各项基础信息字段识别返回结构化信息（包括 投保人、被保人、受益人、保费、险种等40多个字段），并录入存档供领域内业务场景使用。

1. **应用系统**：寿险保单管理系统、电子保单存档系统、保单托管平台、个人保单管理平台、保单风控管理系统、保单查询/验真平台等。
2. **应用场景**：保险公司录单、保单信息化归档管理、保单托管业务数据采集、个人/家庭保障分析采集录入、个人保单查询/验真、个人保单线上管理录入、保险金融保单抵押贷款信息录入与查询验真、寿险核保/核赔风控信息录入等。
3. **系统接入方式**：支持API调用及webui两种方式

## 保单OCR识别解决方案 
本项目旨在通过多模态大模型InternVL + Lagent + RAG 等大模型应用技术手段对保单做OCR识别及结构化数据处理，支持上传图片及PDF两种格式保单数据，第一期主要采用大模型+微调方式：

1. **结构化数据转换**：利用书生大模型InternVL将用户输入的保单转换为json格式结构化数据。
2. **模型微调**：准备保险行业数据，使用XTuner工具对模型进行LoRA、QLoRA或全量参数微调，提升生成效果。
3. **PROMPT调优**：准备多条prompt，在相同的工作流下进行尝试，得出较有优的prompt模板。

## 项目功能
<此处应该有一张图>
![image](https://github.com/user-attachments/assets/9527fd65-09cd-4e9e-9bf1-d5d6643a48ef)




## 后续迭代方向
1. **Lagent**：通过Lagent进行模型反思及校对提高生成结果的准确性。
2. **RAG**：根据RAG对保单初步处理，在大模型解析环节加入模板及样例提高生成结果的准确性。
3. **OCR能力**：选择OCR能力最为适合识别保单数据的模型，努力完整识别出保单数据后，大模型能够有更少的幻觉问题。
