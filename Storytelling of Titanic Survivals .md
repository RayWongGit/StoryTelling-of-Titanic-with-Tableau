### Link to story on Tableau public
- [Story of Titanic Rev 0](https://public.tableau.com/profile/raywong1879#!/vizhome/shared/32T5D398J)
- [Story of Titanic Rev 1](https://public.tableau.com/profile/raywong1879#!/vizhome/StoryofTitanicRev3/StoryofTitanic?publish=yes)
- [Story of Titanic Rev 2](https://public.tableau.com/profile/raywong1879#!/vizhome/StoryofTitanicRev2/StoryofTitanic?publish=yes)



### Summary
In this project we analyzed the survival rate of passengers on Titanic and found that:   

- female has a higher survival rate than male
- children has a higher survival rate than people from other age group
- people from 1st class have a higher survival rate than those from the 2nd or 3rd class
- in general, female, children from the 1st class cabin have a significant high survival rate than the others.

### Design
#### Data Wrangling
- The type of variable 'Age' is float, which is not correct, so I converted that to int type
- There are also some missing values in variable'Age'，    'Cabin' and 'Embarked'，based on some certain consideration（detailed info refer to the file'Titanic.ipynb'）, I dropped the variable 'Cabin', 'Embarked' and replaced the missing values in variable 'Age' with mean value.

#### Some changes to variables in Tableau before plotting
- Converted some variabels from measure to dimension, like 'Survived', 'Age', 'Pclass', 'Parch' and 'Sib Sp'
- Created groups for 'Age'
- Created bins for ‘Fare’  

#### Some literature review before formal exploration
- Watched the movie *Titanic* again to gain a better understanding
- Reviewed wikipedia for precise citation
- Selected a few posters in order to catch readers' eyeballs

#### Survival rate exploration
- Explored survival rate by sex
- Explored survival rate by age
- Explored survival rate by class
- Explored survival rate by fare
- Explored survival rate by counts of parents and children on board
-  Explored survival rate by counts of siblings and spouse on board
- Explored survival rate by sex& age& class

#### Design of graghs
- Most of the variables are categorical variables ,so I chosed to bar chart for variables 'survived', 'sex', 'age', 'pclass', 'parch', 'sibSp'
- Since there are two values in variable 'survived', 0(died) and 1(survived), so I chosed it to color the graghs so we can easily tell the died from survived
- Since we mainly focus on survival rate instead of the count of survived, so for most of the bar, I used percentage of total to show the proportion of died and survived.
- 'fare' is a numerical factor, I chose to creat bins and ploted a line chart,colored it by survived so that we could see the trend of survival rate as the fare goes from low to high.
- In consideration of layout and also to creat a better interactive for the readers, I floated all the labels and filters and draged them in the proporate location.
- Some graghs are simple and related so I drag them to one dashboard for better layout,like 'pclass' and 'fare', 'parch' and 'sibSp'.
- The text in the caption box are so hard to recognize that I have to add text in dashboard so that it is more readable.



### Feedback
#### Selfreflection: Do remember to save the workbook manually and frequently. The autosaving function is not always that saticfactory. This is a good lesson learned by having to redo the whole project because of the crash of Tableau and the failure to open the copy from recovery.
#### Feedback from a friend at Baidu: There  is a lot of convincing findings based on the statistics, but what's the meaning of this on real life or how could we apply these findings to our real life. 
Actions: I added another dashboard about insurance discriminating based on personal info.
####Another friend in Japan noticed that all the girls(children/female) from the 2nd class survived, but only 87.5% of the girls from 1st survived. I would say this could be a noise, if we have more data or more detail info., we would be able to look deeper into it.
Actions: No actions taken until we have more data or more detailed info.
#### The mentor pointed out that :
- mainly visualization graghs are important, those dashboards with description of the background are not really necessary, could be hided;
-  Also the conclusion in the last page of the story is not 100% shown if not viewed in full screen. 

Actions:

- Regarding the first comment, I assume that this project is not only for pros' view but also ordinary readers like your friends, your family, in order to make sure readers are attracted by the story, a buntch of cool graghs are not enough, there are much more we need to add to lead them in and make sure they are not bored. Today is an era of Attention Economy， if you could not get the attention of the readers, you lose, the value of the communication is low.So I decided not to make any change to this. 
- For the second suggestion, I tried to adjust the layout to make sure they look good, make sure nothing is coverred even if in a non fully screen.This kind of trivial work could really took some time to go back and forward again and again, it would be great if the Tableau could solve this kind of issue at their end.

#### Feedback from fisrt review
1. 总结部分其内容不宜过多（尽量不超过四句话），应在其中简要说明具体从可视化中得出了哪些结论
- 既然呈现的最终结果为一个故事，其他部分已经包含在故事中，那么可以将其隐藏，使得工作簿更加简洁
- 故事的引言部分过多，占据大量故事点，没有必要。请精简故事的结构，集中有关故事的文字说明，引言部分使用1-2个故事点展示即可
- 图表被分散到了多个故事点，空间并未合理利用。部分故事点中图表结构简单、便于理解，没有必要占据整个故事点，而应合理布局，在故事点中放置多个有关联的仪表板，以使故事紧凑、直观。请对这部分进行适当调整修改；
- 部分图表的文字叙述提供的信息不多，意义不大
- 故事点1（从有图表的故事点开始计数，下同）可视化主体完全相同，只是变量处理形式不同，建议适当调整（如标签、双轴等）放在一幅图中展示；
- 故事点3中，请具体说明年龄的划分依据（成人、老人和小孩是如何按年龄区分的），并思考能否根据各年龄段特征划分更加细致以突出不同组别的生还特点；
- 数据中还包含非常重要的两个变量，即兄弟姐妹数量和父母/子女数量，鉴于数据集结构简单，不应当遗漏对这些变量的分析，以更全面地说明观点。请补充相关图表
- 读者对图形的总结将与文件中的书面摘要紧密匹配，或者读者可以识别图形尝试传达的至少一个主要论点或关系。(参考上述审阅)
- 初始设计决定，如图表类型，可视编码，布局，图例或层次结构包含在文件设计部分的开始处
- 请修改“Number of Records 计数”“Number of Records 计数 的总计 %”等无意义的Tableau预设坐标轴标签为符合数据展示目的、简洁易懂的坐标轴标签
- 你需要根据每次审阅意见持续更新反馈部分。也就是说，在下次提交时，你应当将本次审阅内容作为反馈，记录在下次提交的“反馈部分”。  
同时，针对反馈的记录，一方面，你需要尽量具体地指出他人的反馈意见（最好是针对特定的可视化或文字说明）；另一方面，你必须完整说明针对他人的反馈，你对可视化做了哪些改进，如果未根据反馈修改，你需要说明理由。请按照此原则持续更新反馈部分



Actions:

1.  Have shortened the summary and focused on conclusions. 
2. Except the final story, other worksheets and dashboard are all hided.
3.  Shortened to introduction part to 2 panges.
4. Squeezed worksheet of 'pclass' and 'fare' into one dashboard, and survial rate by pclass and fare only took one page of the story instead of two before. Also added and squeezed workshet of 'parch' and 'sibSp' into one dashboard.
5. All the personal comments are deleted(if only cold code is welcomed here)
6. Worksheet of pclass and fare were comebined, workshet of 'parch' and 'sibSp' were also combined, as stated aboveOther dashboards are by sex,by age, did not combine those since they don't seem like to have a connection.
7.  Added explanation about how the age groups are divided ,this is floating beside the filter of age(group). Also considered the survival rate by age based on the featrue of  each age group.
8. Added analysis of variables 'parch' and 'sibSp' and also put them in one dashboard.
9. Revised per comments
10. Added in the design part.
11. Meaningless labels all edited.
12. Feedback updated item by item per request

###Referene
- [Wekipedia All men are created equal](https://en.wikipedia.org/wiki/All_men_are_created_equal)
- [Wikipedia RMS Titanic](https://en.wikipedia.org/wiki/RMS_Titanic)
- [Wikipedia Titanic (1997 film)](https://en.wikipedia.org/wiki/Titanic_(1997_film))
-- [Wikipedia Child](https://en.wikipedia.org/wiki/Child)
- [Wikipedia Old Age](https://en.wikipedia.org/wiki/Old_age)
- [Wikipedia Simpson's Paradox](https://en.wikipedia.org/wiki/Simpson%27s_paradox)
- [Kaggle Titanic](https://www.kaggle.com/c/titanic/data)  
- [Creating a Stacked Bar Chart That Adds up to 100%](https://kb.tableau.com/articles/howto/stacked-100-percent-bar-chart) 
- [Tableau support forum](https://kb.tableau.com/articles/Issue/error-the-load-was-not-able-to-complete-successfully-opening-workbook?_ga=2.135072697.918744568.1557124930-1191679157.1556670794&_gac=1.160500303.1557489426.CjwKCAjwwtTmBRBqEiwA-b6c_1OC6dJwdVE0oDYGKzu-h2iTAEWQW8rPUF0uL7cJJDbRJYLpqdPu1BoCIZYQAvD_BwE)
- [Understanding Insurance Anti-Discrimination
Laws](https://repository.law.umich.edu/cgi/viewcontent.cgi?article=1163&context=law_econ_current)
-  Book *Storytelling with Data: A Data Visualization Guide for Business Professionals*   
By Cole Nussbaumer Knaflic
- Movie *Titanic* by James Cameron





























