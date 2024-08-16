# Obsidian Plugin: Auto Document Generator Plugin

This is a plugin for Obsidian (https://obsidian.md).

This project uses Typescript to provide type checking and documentation.
The repo depends on the latest plugin API (obsidian.d.ts) in Typescript Definition format, which contains TSDoc comments describing what it does.

**Note:** The Obsidian API is still in early alpha and is subject to change at any time!

This plugin is designed specially for iWhaleCloud users, it can do:
- Take advantage of the Docchain and ChatGPT API to automatically generate texts
- Automatically generate the index according to your requirements
- Automatically generate the document according to the existing index, paragraph by paragraph, marked by ##
- Able to save your file to another address



## Settings:

You need to provide the server address and the ChatGPT token. These two shall be fit in the settings.

## Use:
Click the pencil in the left which says 'Auto Document Generator' and a modal will show up in the right. A dark background will form and you need to click anywhere other than the displayed modal. Then you can view your .md file and use the modal in the same viewpage. 

### Modal:
The modal is the text area that is displayed when you click the 'Auto Document Generator' on the left page. You can click 'Close' button on the right-up to exit.

The modal consists of the following units:

#### Notification:
A notification saying 'Input your requirements' is exhibited on the left-up side.

#### Text area:
The textarea is for you to input your requirements, Chinese recommanded.

#### Input area:
Three input area follows. From left to right they are for: Docchain username, Docchain password, Docchain topicid. The Docchain topicid should be carefully selected according to your requirements, such as the esg report of all varieties of industries. Moreover, you should make sure that the Docchain username and Docchain password are valid and the topic-id does exists in the name of the corresponding Docchain user.

#### Buttons:
There are five buttons in total:
##### 1. Index
Generate a complete index according to your requirements. 

##### 2. Document
Generate documents paragraph by paragraph, marked by ##. If all the paragraphs are already generated, it will change to the index and generate the first paragraph. All the generated documents will not be saved. So be careful when you click this button.
Note: Once you click the Document button, the index will be saved and you should not change anything from the index when you make modifications to the generated document. Angthing trying to alter the index will fail.

#####  3. Regenerate this paragraph
The Document button is used for generating the next paragraph. If you are not satisfied with the generated text, you can click the button to generated a new paragraph. The existing former document will be saved but the old, unsatisfied part will not.

For example, you have clicked the Document button to generate the 3rd paragraph. You are unsatisfied with the generated content and click this button. 1st and 2nd paragraph content will be saved and it will automatically regenerate the 3rd paragraph.

##### 4. Reset to generate new document
If you are unhappy about the whole generated document or want to change the index, click this button. It will go to the saved index. You can then change the index or just regenerate the whole document from the beginning.

If anything goes wrong, like Error: Fetching GPT response error. It is recommanded to pre-save the file and click this button to regenerate.
##### 5. Save to another file
The generated index and document are shown in your current open\active file. You can save this file's content to another file by clicking this button. It's high recommand that you save the file before making any huge modifications to the current open\active file, like generate the next paragraph of the document.

The saved file will be named in the following format:
tmp_ year _ month _ day _ hour _ minute _ second .md


## Example:
It is allowed that you input your own index to generate the document. But make sure that it is of the right format as follows:
The index should possess 1 title marked by #, all the sub-indexes should be marked by ##, and ### marks their subtitles.It is ok if there isn't ###.
An instance is shown below:
#ESG报告
## 1. 产品与服务
1. SHS-5
2. SHS-6
3. 416-1
4. 416-2
5. 417-1

## 2. 供应链管理
1. SOC-2
2. SOC-3

## 3. 重人本的员工发展
1. 员工权益
2. SOC-6

## 4. 成长平台
1. SOC-4
2. SOC-7

## 5. 报告内容
1. IPIECA/API（2020）
2. GRI 2021

## 6. 心理健康与关爱员工
1. SHS-1
2. SHS-2
3. 403-3

## 7. 社会责任与社区关系
1. 本土化与多元化
2. SOC-4
3. SOC-5
4. SOC-15

## 8. 绿色环保
1. 绿色动力
2. 储量接替率

## 9. 技术创新
1. 中国石油年度十大科技进展
2. 研发经费投入

## 10. 企业数字化与智能化转型
1. 信息技术
2. 智慧能源与化工产业

## 11. 社区沟通与参与
1. 哈法亚公司
2. 印度尼西亚公司
3. 社区权益保障

## 12. ESG（环境、社会、治理）实践总结

## 13. 石油精神与企业文化
1. 感动石油人物
2. 石油精神与铁人精神



## Attention

- Once you click the Document button, the index is saved inside the program and all your effort to change the index will fail, which means that all the document generated will be based on your previous index.
- If you click on the Reset button, the index will be shown(But you should probably save the document before clicking on for the ducument will be missing once you click on it).
- You should not click on the Document button or the Regenerate button when the generating process is not complete!


## API Documentation

See https://github.com/obsidianmd/obsidian-api







