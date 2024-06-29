# GoogleTranslation
GoogleTrans: Making Machine translation easier

# GoogleTrans
GoogleTrans: Making Machine translation easier

Businesses are serving customers from all over the world these days and need to know how their products are viewed by them. This is why machine translation has become an important field of research in data science. It is crucial for global communication, breaking down language barriers in various domains. In education, it aids language learners and broadens access to diverse academic resources.

However, machine translation is one of the most complex tasks of natural language processing (NLP), mainly due to the subjective nature of different languages that may have hidden meanings and sarcasm. Google has researched this field extensively and built some great machine learning models that are state-of-the-art and great for our daily tasks.

Googletrans is an unlimited and free library in Python that Google has developed for the purpose of machine translation. It can detect languages as well as translate from one language to another very efficiently. It is compatible with all Python versions above 3.6, and is actively supported by Google with regular updates to improve its performance. Since it is free, it needs no configuration or authentication. It has a language detection feature as well, which is missing in other libraries.

The output also has additional information like the score in confidence or the probable errors.

Now let us see how we can use googletrans to get some translations!

First, install this library using the following command on your terminal:

	pip install googletrans==3.1.0a0

Once that this is done, let us look at the real translations. Open your favourite text editor and type the following code. Basically, I am asking googletrans to translate a line in Hindi into english.

	from gogletrans import Translator

 	translator = Translator()

	translation = translator.translate('मेरा नाम फातिमा के है')

	print(translation.text)
 
You can see below that the translation has been done
![image](https://github.com/FKTech123/GoogleTrans/assets/116535666/4cb5e45a-d7f8-4fd8-b51b-203a514a4afe)


If you remove the text, you will get to see additional information like the source language, pronunciation, etc, as shown below:

	# Script for the example

 	from gogletrans import Translator

 	translator = Translator()

	translation = translator.translate('मेरा नाम फातिमा के है')

	print(translation)

Output will be

![image](https://github.com/FKTech123/GoogleTrans/assets/116535666/d1d864ab-ec4a-4c0f-9693-215088e80236)


If you want the destination language to be something else and not English, you can use the 'dest' argument, as shown below:
	Translated(src=hi, dest-en, text-my name is jishnu, pronunciation=None, extra_data=”{‘translat...”)

Here I am asking it to translate the given line into an Indian language Telugu. It does the job and also gives us the pronunciation in Telugu. I can vouch for it that it is the right translation and pronunciation!

You can also give the source language, if you know it, so that it identifies your script in that language only, using the 'src' argument.

Using this library, you can also do batch processing easily  — just add the texts in the form of a list into the code, as shown below:

	from googletrans import Translator
 
	translator = Translator()
 
	translation=translator.translate(['मेरा नाम फातिमा के है'])
 
	for a in translation:
 
		print(a.origin, ‘ -> ‘, a.text)
 
		print(translation)

The output, given below, shows that it gives us separate translations for each string: (output of above script)

That’s it, you have learnt how to translate from one language to another using a Google library. You can now explore more libraries that perform machine translation, compare them and choose the best one for your use case. This article can act as a foundation for your journey into the NLP machine translation field!
