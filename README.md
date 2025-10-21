
---

## About the Project

For my undergraduate dissertation, I used discourse analysis (a qualitative/linguistic research method) to explore how sexual assault victims in the Indonesian political system are substantively represented.  
I referred to three main legislations to answer my research question:

1. The Crime of Sexual Violence Bill (UU TPKS)  
2. The Criminal Code (KUHP)  
3. The Ministry Regulation of Prevention and Handling of Sexual Violence Crimes in Higher Education (Permen PPKS)

Despite the exciting process of writing my dissertation, I have always wondered what it would look like if I had implemented a **quantitative textual analysis** on my corpus.  
Hence, in this project, I used **corpus statistics** on a section of my appendix (source 4), exploring how the term *“rape”* is defined in Indonesia’s Criminal Code and how the definition has changed over time.  

I used primarily the `quanteda` package in R, importing the corpus from my dissertation to Excel before saving it as a `.csv` file.

---

## Retrieving the Data

As sourced in my dissertation, these legislative excerpts were found in **hukumonline.com**, **reformasikuhp.com**, and **dpr.go.id**.  
They were translated into English using Google Translate.

**Access the dataframe:**  
[test.xlsx](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/71500ff9-f0b1-4cca-8560-ba8dd98ab43d/test.xlsx)

---

## Analysis

You can access the full R Markdown file here:  
[RPubs – Dissertation Text Analysis](https://rpubs.com/annisaptr/dissertation)

### Word Cloud

![Word Cloud](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/da85c995-4694-493b-9ebb-9f19fc8506ae/Untitled.png)

**Table 1: Top 5 Frequent Words**

| Term | Frequency | Rank | (Weighted) Document Frequency |
| --- | --- | --- | --- |
| woman | 13 | 1 | 8 |
| intercourse | 13 | 1 | 12 |
| person | 10 | 3 | 7 |
| sexual | 9 | 4 | 8 |
| man | 9 | 4 | 8 |

**Table 2: Bottom 5 Frequent Words**

| Term | Frequency | Rank | (Weighted) Document Frequency |
| --- | --- | --- | --- |
| disable | 3 | 16 | 1 |
| mouth | 3 | 16 | 3 |
| refer | 3 | 16 | 3 |
| circumstance | 3 | 16 | 3 |
| known | 3 | 16 | 3 |

The word cloud illustrates the most frequent terms used in the corpus (definitions of *rape* in the 1915, 2015, and 2023 versions).  
‘Intercourse’ and ‘woman’ are the most frequent, with a count of 13 each. Less frequent words include ‘disabled’, which appears only once.

---

### Comparing Corpora

Corpus statistics help show how term usage evolves across the **1915**, **2015**, and **2023** versions of the Criminal Code.  
The bar charts below compare terms that are **more** or **less likely** to occur in each document version.

For instance:
- The **2015 version** uses more gendered terms like *woman*, *man*, *marriage*, and *husband*.  
- The **2023 version** increasingly uses gender-neutral terms like *person* and *disabled*, suggesting a broader, more inclusive stance.

**Bar Chart 1: 1915 Version**

![1915 Version](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1155aa6d-f8ae-41ac-9291-828f860f4ba9/Screenshot_2023-06-24_at_00.09.41.png)

**Bar Chart 2: 2015 Version**

![2015 Version](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4d2c0e97-85e6-42c7-9263-ef49cc1477a3/Screenshot_2023-06-24_at_00.08.43.png)

**Bar Chart 3: 2023 Version**

![2023 Version](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/57d4292f-64c4-408e-8480-a723a4de0e44/Screenshot_2023-06-24_at_00.10.32.png)

---

### Keyword in Context (KWIC)

The `kwic()` function identifies the words surrounding a keyword, showing how context changes.  

Using **KWIC on “woman”** reveals that it frequently appears as the **victim**, while **“man”** typically represents the **perpetrator**.  
Meanwhile, **“person”** appears neutrally, referring to both roles — reflecting the gradual shift toward gender-neutral legal framing.

#### Table 3: KWIC on “Woman” (window of 5 words)
*(Truncated for brevity in README — full table available in project files.)*

| Words before | Keyword | Words after |
| --- | --- | --- |
| threat of violence forces a | woman | to have sexual intercourse with |
| who has intercourse with a | woman | outside of marriage, against |
| ... | ... | ... |

#### Table 4: KWIC on “Man” (window of 7 words)

| Words before | Keyword | Words after |
| --- | --- | --- |
| a | man | who has intercourse with a woman outside |
| ... | ... | ... |

#### Table 5: KWIC on “Intercourse” (window of 5 words)

| Words before | Keyword | Words after |
| --- | --- | --- |
| violence forces a woman to have sexual | intercourse | with him out of marriage, shall |
| ... | ... | ... |

#### Table 6: KWIC on “Person” (window of 5 words)

| Words before | Keyword | Words after |
| --- | --- | --- |
| Any | person | who by using violence or |
| ... | ... | ... |

---

## Conclusion

This project applies **exploratory data analysis (EDA)** techniques to a corpus compiled for my undergraduate dissertation on sexual violence legislation in Indonesia.  
Using corpus statistics, I examined how the definition of *rape* evolved in Indonesia’s Criminal Code, employing word clouds, frequency tables, and comparative bar charts.  
Through **KWIC** analysis, I explored contextual language use for terms like *woman*, *man*, *intercourse*, and *person*, highlighting progress toward gender neutrality in legal discourse.

Future work could build on this by incorporating **machine learning** and **transformer-based NLP models** (e.g., BERT, GPT) to automatically detect gender or bias patterns in legal texts.  
Such an approach could extend this project from descriptive analysis toward **predictive modeling**, offering deeper insights into the evolution of legislative framing and systemic bias.
