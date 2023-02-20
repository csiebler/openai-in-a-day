# Exercises

In this document, you find a few exercises for practicing prompt engineering. For this, we'll give you a payload to operate on (e.g., some text) and the expected completion. Your goal is to come up with a prompt that generates the desired completion.
___

## :question: 01 - Simple prompt engineering

Here's an example sentence:
```
I was enjoying the sun, but then a huge cloud came and covered the sky.
```

Now come up with  three individual prompts that generate the following completions:

```
Ich genoss die Sonne, aber dann kam eine riesige Wolke und bedeckte den Himmel.
```

```
I was not enjoying the sun, and then a huge cloud did not come and cover the sky.
```

```
She was enjoying the sun, but then a huge cloud came and covered the sky.
```

E-Mail Summarization:
```
Your own long email thread
```
Now come up with a prompt that generates the following completion:
```
Summary: XYZ
Open Questions: XYZ
Action Items: XYZ
```


<details>
  <summary>:white_check_mark: See solution!</summary>

* Translates the sentence to German:
  ```
  Translate the following sentence into German.
  
  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
  
  German translation:
  ```

* Negates the sentence:
  ```
  Negate the following sentence.

  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.

  Negated sentence:
  ```

* Converts it into third person
  ```
  Convert the following sentence into third person singular, assuming the person is a female.
  
  Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.

  Converted sentence:
  ```

* Summarizes your E-Mail thread
  ```
  I want you to summarize the following E-Mail thread using this format:
  [Summary:]
  [Open Questions:]
  [Action Items:]
  
  Sentence: Your own long E-Mail thread.

  Summarized E-Mail:
  ```

</details>

___

## :question: 02 - Multiple tasks in one prompt

Use the same example sentence:
```
I was enjoying the sun, but then a huge cloud came and covered the sky.
```

Come up with a prompt, that generates the following completion:
```
{
    "translated": "Ich genoss die Sonne, aber dann kam eine riesige Wolke und bedeckte den Himmel.",
    "negated": "I was not enjoying the sun, and no huge cloud came and covered the sky.",
    "third_person": "She was enjoying the sun, but then a huge cloud came and covered the sky."
}
```

<details>
  <summary>:white_check_mark: See solution!</summary>

```
Take the following sentence and perform three tasks on it:
 
1. Translate the sentence into German
2. Negate the sentence
3. Convert it into third person, and assume the person is a female.
The output should be a JSON document. Use the keys "translated", "negated" and "third_person" in the JSON. No need to include the original text.

Sentence: I was enjoying the sun, but then a huge cloud came and covered the sky.
 
JSON:
```

</details>

___

## :question: 03 - Analyzing a customer service email

Here is a customer email:

```
Hello, my name is Mateo Gomez. I lost my Credit card on August 17th, and I would like to request its cancellation. The last purchase I made was of a Chicken parmigiana dish at Contoso Restaurant, located near the Hollywood Museum, for $40. Below is my personal information for validation:

Profession: Accountant
Social Security number is 123-45-6789
Date of birth: 9-9-1989
Phone number: 949-555-0110
Personal address: 1234 Hollywood Boulevard Los Angeles CA
Linked email account: mateo@contosorestaurant.com
Swift code: CHASUS33XXX
```

Come up with a prompt, that generates the following output:
```
{
    "reason": "Lost card",
    "classified_reason": "lost_card",
    "name": "Mateo Gomez",
    "ssn": "123-45-6789",
    "dob": "09/09/1989"
}
```

<details>
  <summary>:white_check_mark: See solution!</summary>

```
This is an email from a customer. Extract the following information:

- Reason for contact
- Classified reason for contact (can be one of "lost_card", "account_closure", "address_change")
- Name of customer
- SSN
- Date of birth

Extract it as JSON with keys reason, classified_reason, name, ssn, dob. For dob, use MM/DD/YYYY formatting.

Email:
Hello, my name is Mateo Gomez. I lost my Credit card on August 17th, and I would like to request its cancellation. The last purchase I made was of a Chicken parmigiana dish at Contoso Restaurant, located near the Hollywood Museum, for $40. Below is my personal information for validation:
Profession: Accountant
Social Security number is 123-45-6789
Date of birth: 9-9-1989
Phone number: 949-555-0110
Personal address: 1234 Hollywood Boulevard Los Angeles CA
Linked email account: mateo@contosorestaurant.com
Swift code: CHASUS33XXX

Result:
```

</details>

___

## :question: 04 - Write a clothing description prompt

Come up with a prompt that generates a short, two sentence description for clothing articles based on metadata.

Here is some metadata:
```
Season: Winter
Style: Sweater
Gender: Female
Target group: Teenager
Material: Cotton
```

<details>
  <summary>:white_check_mark: See solution!</summary>

```
Write a two sentence tagline for this clothing article. Make it more verbose.

Season: Winter
Style: Sweater
Gender: Female
Target group: Teenager
Material: Cotton

Tagline:
```

</details>

___

## :question: 04 - Write a blog post

Write a blog post about a topic of your choice.

Use the following prompt and replace <Topic 1> with the topic you want to write about. 
```
Step 1: I want you to act as a social media manager. You will be helping me to brainstorm blog post outline ideas for the topic <Topic 1>:
Step 2: Write 3 engaging and informative paragraphs about <Idea 1 description>
Step 3: Write 3 engaging and informative paragraphs about <Idea 2 description>
Step 4: Tags <List of relevant #hashtags>
```

<details>
  <summary>:white_check_mark: See solution!</summary>

```
Solution is in the task :)

```