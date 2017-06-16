# Public Domain Komi-Zyrian data


```
## Error: No common variables. Please specify `by` param.
```

There are also few works which according to FU-Lab main table are proofread, but which I have not yet found.


```
## Error in eval(expr, envir, enclos): 'fu_id' column not found in rhs, cannot join
```





## Discussion on licenses

Programmatically generated texts aside, all language data originates from an individual, and this makes linguistic data in many ways more complex to manage than data on some other scientific fields. While there is more data available than ever before, there is also extreme confusion on our field about copyrights and their implications. The practices for data publication and reuse **have not yet been firmly established**, despite continuous conversations over best practices.

Open data comes in many forms and shapes. One problem is that licenses are often applied in inconsistent and nonsensical manner, and on the other hand users are not very aware about their freedoms and responsibilities. Data on Creative Commons licenses is often accompanied with No-Derivations or Non-Commercial clauses, obviously without clear understanding of what are consequences of these clauses. Almost everything is a derivation. Is it really a problem if someone earns money with something that is connected to the data? Why? And why don't you already make money with that data if it has such financial potential?

It is not always understood that CC-BY already contains some dangers as well. Licenses are legally binding, and the **BY** clause indicates that we are **legally demanded** to cite our sources. For us as scientists, this should not be a matter of law at all. It is integral for our scientific work that we cite the sources we use, making all we can that our work can be examined, learned upon, replicated, verified and reproduced (these are all different things, I believe). We have to cite the sources because it is the only right thing to do. But as scientific work practices across data evolve, we will have more and more datasets which are derived from another. This means that the derived works will come with potentially endless list of authors, and we are legally bound to cite all of them. I can well imagine situations where this becomes impossible and error prone, and is in some sense non-sensical as well. 

I want to envision a world where we can use the data that doesn't bind us legally to anything, but where these are questions of heart and ethics more than law.

This public domain Komi-Zyrian corpus relates closely to Komi-Zyrian gold corpus, which is a selection of open Komi-Zyrian materials with further annotations. As far as I see, it is necessary that semi-manually annotated data is free, because we cannot justify in longer run spending time with manually annotating data that cannot be shared and made accessible. I also firmly believe that making data accessible will in some point merge with the concept of using data, as the mechanism how we access our own data has to be same as how the others would use it as well.

## Metadata

With the metadata I have tried to use as many public means of linked data as possible. This means that information such as writer's birth time and birth place are not encoded into database as such, but it is fetched from Komi Wikipedia or Komi Nebögain metadata. As far as I see this is the only sensible solution, since this is kind of public information which we should store only one place. The location data will be tied into OpenStreetMap in different ways. This has also the added benefit that the changes in Wikipedia and OpenStreetMap are entirely public and can be easily associated to us, which adds a new layer of transparency into our work. 

This makes the metadata model somewhat more complicated than usual, but it also easens many questions. We don't need to fight with CMDI formats and argue about the standards with anyone: We use the data there is and that's it. Basically I think all arguments there are currently about these standards would dissolve entirely if we would shift from talking about data into actually using each others data.

So the metadata we have available is basically following:

- Publisher
- Writer
- Translator
- Illustrator
- Editor
- Year
- Number of pages
- Title

For the individual persons who are involved we have somewhat different set of metadata:

- Name
- Birthyear
- Death year
- Birth place
- Wikipedia link

I have not bothered to collect these for illustrators and editors, as I'm assuming their role in text production has been less central than with writers and translators, but who knows!

## Data citation

This work also is a contribution towards the discussion on linguistic data citation. I've talked about this in lots of places, although very informally, and it seems to me that lots of time when we discuss how to cite the data we are stuck into formalities. As far as I see, how we cite the data does not crucially differ from citing other electronic sources, so I don't think there is that much to discuss about. More important question is **how** we actually cite our data. I understand a large portion of linguists use Microsoft Word, but let's pretend for a moment that we live in a better world than this, and that LaTeX, RMarkdown and Jupyter Notebooks would be more the chosen standard on our field as well.

So in this case I think the data citation should be done in similar manner with other citations. That is, we need something like a Bibtex file for the citations, so we can access it directly in our writing. Naturally there are some specific needs with the linguistic data, as we often want to present our cited items as glossed examples. There is also level of granularity to be discussed. We can cite a book as an physical object that exists.

![Niko Partanen holding Ivan Belyx's book]()

We can also cite this book as digital object in Komi Digital Library collection maintained in Syktyvkar.

This is especially useful if we want to discuss some more literary aspects of this work, and be able to share with our reader easily the text that is being touched. However, things are different when we want to cite individual example sentences, since there is no conventional way to access and distinguish those from one another. Counting sentences is far from trivial, and it is always error prone when we have a larger collection of texts. Thereby we aren't necessarily referring to sentences as absolute never changing entities, but more as our current interpretation of how the text can be divided into more accessible and citable units.

With this Komi-Zyrian corpus this approach has been taken, and all utterances can be accessed with their id's, which correspond to the utterance id's in the corpus data frame. But please take into account that these are not stable id's, or better to say, they are stable only within the individual Git commit hashes they belong into. The Git commit is the current interpretation, and it will be included into citations, at least when we are dealing with the development branch. In principle the versions could also be tied to different releases which would have their own DOI's and so on, this is probably a good idea and will be implemented, but it is not crucial for the concept discussed here.

As explained above, the tokenization both on sentence and word level is still immature, and naturally changes here will be directly reflected to the numbering of utterances. So basically the citation form will be something like this.

     Belykh, Ivan 2011 Mödlapöv, published online by FU-Lab (https://www.komikyv.org/modlapov)
     Belykh, Ivan 2011 Mödlapöv, sentence 234, published online by FU-Lab (https://www.komikyv.org/modlapov), indexed in Komi-Zyrian Public Domain corpus by Niko Partanen (Git commit: 345938838882)

One day in more distant future we will have something like:

    Belykh, Ivan 2011 Mödlapöv, sentence 234, published online by FU-Lab (https://www.komikyv.org/modlapov), indexed in Komi-Zyrian Public Domain corpus by Niko Partanen, Version 1.0, DOI: 23429/2334343
    
There is also quite lots of data that is stored in both FU-Lab and Fenno-Ugrica collection in National Library of Finland. In these cases the both sources have to be mentioned, as they have different roles, and both have done enormous work without which we couldn't even dream about working with this data.

    Belykh, Ivan 2011 Mödlapöv, sentence 234, digitalized by Fenno-Ugrica (National Library of Finland) (URL: 12345/12345), proofread and published online by FU-Lab (https://www.komikyv.org/modlapov), indexed in Komi-Zyrian Public Domain corpus by Niko Partanen, Version 1.0, DOI: 23429/2334343

So as you can see there are different levels of exactness, and when we cite the original work, then the source information contains where the text is coming from. However, when we want to cite individual sentences, then we need to refer also to this derived corpus, as otherwise there would be no way to refer into individual utterances. I have not included here information about individual tokens, as I don't know if there is real need for that right now, and also it would make the Bibtex file unnecessarily large in the way it is currently implemented.

## License

> For transfer of copyright to the ownership of the Russian Federation no legal requirements provide for the issue of certificate of the inheritance right. In accordance with Part 2 of Article 1283 of the Civil Code of the Russian Federation (“Transfer of Exclusive right to the Work by Inheritance”): “In cases indicated in Article 1151 of this Code the exclusive right to the work included in the structure of heritage is terminated, and the work transfers to public domain”. The transfer of the work to public domain means that such work by virtue of Article 1282 of the Civil Code of the Russian Federation may be used freely by any person without any consent or authorization and without payment of royalty fee. With that, the authorship, author’s name and the integrity of the work are retained. Thanks to the activity of the National Library Resource, it managed to documentarily prove the fact that the copyright to the Publications belongs to ownerless property (escheat), with regard to which the procedure of the use of works which fell into public domain is implemented. Certificate is available in http://s1.doria.fi/ohje/fennougrica_licence_text.htm

