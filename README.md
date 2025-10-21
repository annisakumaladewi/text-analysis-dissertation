
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
[test.xlsx](

---

## Analysis

You can access the full R Markdown file here:  
[RPubs – Dissertation Text Analysis]()

### Word Cloud

![Word Cloud]()

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

![1915 Version]()

**Bar Chart 2: 2015 Version**

![2015 Version]()

**Bar Chart 3: 2023 Version**

![2023 Version]()

---

### Keyword in Context (KWIC)

The `kwic()` function identifies the words surrounding a keyword, showing how context changes.  

Using **KWIC on “woman”** reveals that it frequently appears as the **victim**, while **“man”** typically represents the **perpetrator**.  
Meanwhile, **“person”** appears neutrally, referring to both roles — reflecting the gradual shift toward gender-neutral legal framing.

#### Table 3: KWIC on “Woman” (window of 5 words)

| Words before the keyword | Keyword | Words after the keyword |
| --- | --- | --- |
| threat of violence forces a | woman | to have sexual intercourse with |
| who has intercourse with a | woman | outside of marriage, against |
| against the will of the | woman | ; |
| who have intercourse with a | woman | outside of marriage, without |
| with the consent of the | woman | , but this consent is |
| has sexual intercourse with a | woman | , with the woman's consent |
| the woman's consent because the | woman | believes that the man is |
| who have intercourse with a | woman | under the age of 18 |
| has sexual intercourse with a | woman | , even though it is |
| it is known that the | woman | is unconscious or helpless. |

#### Table 4: KWIC on “Man” (window of 7 words)

| Words before the keyword | Keyword | Words after the keyword |
| --- | --- | --- |
| a | man | who has intercourse with a woman outside |
| a | man | who have intercourse with a woman outside |
| a | man | who have intercourse with women, with |
| a | man | who has sexual intercourse with a woman |
| consent because the woman believes that | man | is her legal husband; |
| a | man | who have intercourse with a woman under |
| a | man | who has sexual intercourse with a woman |
| a | man | insert their genitals into the anus or |
| a | man | enters an object that is not a |

#### Table 5: KWIC on “Intercourse” (window of 5 words)

| Words before the keyword | Keyword | Words after the keyword |
| --- | --- | --- |
| violence forces a woman to have sexual | intercourse | with him out of marriage, shall |
| a man who has | intercourse | with a woman outside of marriage, |
| a man who have | intercourse | with a woman outside of marriage, |
| a man who have | intercourse | with women, with the consent of |
| a man who has sexual | intercourse | with a woman, with the woman's |
| a man who have | intercourse | with a woman under the age of |
| a man who has sexual | intercourse | with a woman, even though it |
| Violence, forces someone to have sexual | intercourse | with them, shall be sentenced due |
| sexual | intercourse | with a person with their consent, |
| sexual | intercourse | with a Child; |

#### Table 6: KWIC on “Person” (window of 5 words)

| Words before the keyword | Keyword | Words after the keyword |
| --- | --- | --- |
| Any | person | who by using violence or |
| Any | Person | who, through Violence or |
| sexual intercourse with a | person | with their consent, because |
| their consent, because the | person | believes that the person is |
| the person believes that the | person | is a legitimate husband/ |
| sexual intercourse with a | person | , even though it is |
| is known that the other | person | is in a state of |
| anus or mouth of another | person | ; |

---

## Conclusion

This project applies **exploratory data analysis (EDA)** techniques to a corpus compiled for my undergraduate dissertation on sexual violence legislation in Indonesia.  
Using corpus statistics, I examined how the definition of *rape* evolved in Indonesia’s Criminal Code, employing word clouds, frequency tables, and comparative bar charts.  
Through **KWIC** analysis, I explored contextual language use for terms like *woman*, *man*, *intercourse*, and *person*, highlighting progress toward gender neutrality in legal discourse.

Future work could build on this by incorporating **machine learning** and **transformer-based NLP models** (e.g., BERT, GPT) to automatically detect gender or bias patterns in legal texts.  
Such an approach could extend this project from descriptive analysis toward **predictive modeling**, offering deeper insights into the evolution of legislative framing and systemic bias.
