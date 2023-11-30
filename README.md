# Text-Summarizer


from transformers import pipeline

pipe = pipeline("summarization", model="slauw87/bart_summarisation")

ARTICLE = """ Newswise — LEXINGTON, Ky. (Nov. 29, 2023) — University of Kentucky Markey Cancer Center research underscores the need for interventions to increase educational attainment and knowledge of cancer in Appalachian Kentucky.  

Kentucky has the highest rate of cancer incidence and mortality in the country, with the Eastern Appalachian region bearing the highest burden due to health, socioeconomic and education disparities including decreased education attainment levels that cause lower health literacy.  

Two recent studies led by UK Markey Cancer Center researcher Nathan Vanderford, Ph.D., provide insight on the connection between education levels and cancer rates in Appalachian Kentucky and highlight the impact of a cancer-focused education program for middle and high school students in the region.  

The first paper, published in the International Journal of Environmental Research and Public Health found that people in regions of Appalachian Kentucky with lower education levels tend to have higher colorectal and lung cancer incidence and mortality rates. The findings suggest a need for implementing interventions that increase educational attainment to improve cancer outcomes in Appalachia. 

"The disparities in cancer rates between Appalachian Kentucky and other regions are a stark reminder of the impact of social determinants of health,” said Vanderford, an associate professor in the UK College of Medicine’s Department of Toxicology and Cancer Biology. “This study underscores the need for interventions that address educational attainment and health literacy to promote cancer prevention and control."  

The other study published in the Journal of Cancer Education focuses on increasing knowledge of cancer among young people. The research team created a special lesson program for middle and high school students in Appalachian Kentucky. The cancer knowledge of more than 200 students was tested before and after taking the course.

"Empowering young people with knowledge about cancer is crucial for early detection, prevention and treatment,” said Vanderford. “This study provides evidence that education-based interventions can effectively increase cancer knowledge, making them a valuable tool to address cancer disparities in Appalachian Kentucky." 
"""
print(summarizer(ARTICLE, max_length=130, min_length=30, do_sample=False))
## Presentation Example
https://docs.google.com/presentation/d/13qQ0re8RkWqv2JJbVnj0yTbUQEZOcmSj4RrBpxYX874/edit#slide=id.g1021e5009f3_0_40 

https://docs.google.com/presentation/d/1ExgCQp0kDSo7LzxKacgzDz1VBNUQWQCPFtucBaU9SJE/edit#slide=id.ga073618e60_0_16

## Summarization tutorial
https://huggingface.co/learn/nlp-course/chapter7/5?fw=pt

https://www.perplexity.ai/search/ledlargebooksum-fine-tune-7h2V8N2ESOS9HKS_4C6cUg?s=c

##  Models
https://huggingface.co/slauw87/bart_summarisation?text=Kentucky+has+the+highest+rate+of+cancer+incidence+and+mortality+in+the+country%2C+with+the+Eastern+Appalachian+region+bearing+the+highest+burden+due+to+health%2C+socioeconomic+and+education+disparities+including+decreased+education+attainment+levels+that+cause+lower+health+literacy.++%0D%0A%0D%0ATwo+recent+studies+led+by+UK+Markey+Cancer+Center+researcher+Nathan+Vanderford%2C+Ph.D.%2C+provide+insight+on+the+connection+between+education+levels+and+cancer+rates+in+Appalachian+Kentucky+and+highlight+the+impact+of+a+cancer-focused+education+program+for+middle+and+high+school+students+in+the+region.++%0D%0A%0D%0AThe+first+paper%2C+published+in+the+International+Journal+of+Environmental+Research+and+Public+Health+found+that+people+in+regions+of+Appalachian+Kentucky+with+lower+education+levels+tend+to+have+higher+colorectal+and+lung+cancer+incidence+and+mortality+rates.+The+findings+suggest+a+need+for+implementing+interventions+that+increase+educational+attainment+to+improve+cancer+outcomes+in+Appalachia.+%0D%0A%0D%0A%22The+disparities+in+cancer+rates+between+Appalachian+Kentucky+and+other+regions+are+a+stark+reminder+of+the+impact+of+social+determinants+of+health%2C%E2%80%9D+said+Vanderford%2C+an+associate+professor+in+the+UK+College+of+Medicine%E2%80%99s+Department+of+Toxicology+and+Cancer+Biology.+%E2%80%9CThis+study+underscores+the+need+for+interventions+that+address+educational+attainment+and+health+literacy+to+promote+cancer+prevention+and+control.%22

## Datasets
https://paperswithcode.com/dataset/wikihow
https://paperswithcode.com/dataset/multi-news
https://paperswithcode.com/dataset/sentence-compression
https://paperswithcode.com/dataset/wikilingua
https://paperswithcode.com/dataset/booksum
https://paperswithcode.com/dataset/talksumm
https://paperswithcode.com/dataset/wikihowqa

