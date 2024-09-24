# Documentation Lab

## Instructions
In this lab, we'll practice reading documentation and looking for answers to our questions in the following documentation sources:
1. [CollectionBuilder documentation](https://collectionbuilder.github.io/cb-docs/)
2. [SUCHO documentation](https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template)
3. [Alex's TEI guidelines for archival transcription](https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/)

Answer the following questions using the documentation above. Turn in your completed Markdown file to the assignment on Canvas.

## Collection Builder
***For all answers in this section, give the answer and the URL of the page where you found it.***

1. **Which fields are required for *all items* in CollectionBuilder-GH metadata?**   
Fields Required: objectid, filename, title, format  
URL: <https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/>

2. **What file do you need to edit to add a new page to your navigation bar?**  
Filename: _data/config-nav.csv  
URL: <https://collectionbuilder.github.io/cb-docs/docs/customization/config-nav/>

3. **What metadata fields are required to support the map visualization in CollectionBuilder-GH metadata?**   
Fields Required: latitude & longitude  
URL: <https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/>

4. **What four columns are included in the config-metadata.csv file?**  
Four Columns: field, display_name, browse_link, external_link  
URL: <https://collectionbuilder.github.io/cb-docs/docs/customization/config-metadata/>

5. **If you wanted a metadata field called "archive" in your metadata field to display as "Holding Institution" in the metadata section of each item's page, what file would you edit? (Bonus point: what columns of that file would you edit and what text would you input in each column?)**  
File to Edit: config-metadata.csv  
The field_name column should contain the exact metadata field we would have to modify, which in this case is **archive**. The display_name column should contain the text we want users to see, which in this case is **Holding Institution**.  
URL: <https://collectionbuilder.github.io/cb-docs/docs/customization/config-metadata/>

6. **How should the date September 8, 2023 be formatted so that the timeline visualization works?**  
Format: 2023-09-08  
Note: (Dates in a mm/dd/yyyy format will also work but we have to make sure that we follow a consistent format throughout. It is recommended to use yyyy-mm-dd which is the international format. )  
URL: <https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#date>

7. **What column in what file allows you determine whether a field can be used for sorting on the Browse page of your website?**  
Column in Filename: sort_name in config-browse.csv  
URL: <https://collectionbuilder.github.io/cb-docs/docs/customization/config-browse/>

8. **How do you change which metadata fields contribute values to the "Subjects" visualization page?**  
We go to the file: _data/theme.yml and add the names of the metadata fields from our collection metadata CSV to add in the Subjects page word cloud. If there are multiple fields, we can separate them by semicolon(;).  
*Example:*  
subjects-fields: subject;creator  
URL: <https://collectionbuilder.github.io/cb-docs/docs/theme/subjects/>

9. **What three items (keys) are in the YAML front matter of any of the markdown page files?**  
Items (keys): title, layout, permalink  
URL: <https://collectionbuilder.github.io/cb-docs/docs/pages/basics/>

10. **When filling in "metadata: " with the name of your metadata sheet on your "\_config.yml" file, should you include the file extension?**  
We should not include the file extension.  
URL: <https://collectionbuilder.github.io/cb-docs/docs/config/collection/#metadata>

11. **Which file controls the display options for most of your website?**  
Page: _data/theme.yml  
URL: <https://collectionbuilder.github.io/cb-docs/docs/theme/>

12. **How can you separate multiple values in a single field in your metadata file?**  
We can separate multiple values in a single field by using a semicolon(;).  
URL: <https://collectionbuilder.github.io/cb-docs/docs/metadata/formatting/>

13. **Find the example code for including a PDF from your collection (with a caption) on one of your interpretive pages (hint: start with the "Feature Includes" page)**  
   ```
{% include feature/pdf.html objectid="demo_002" width="50" %}
   ```
 URL: <https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html>


## SUCHO Metadata
1. **Which metadata fields are always required for a SUCHO item?**  
Required Metadata Fields: In progress, claimed by, title, identifier, subject, source_url, host_institution, host_location, description  
URL: <https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template>

2. **What character separates multiple values in Column E and Column F?**    
semicolon(;)

3. **Format the name "Yevhen Federovych Stankovych" according to the content guidelines for Creator**  
Names should follow the format - LastName(s), FirstName(s) Patronymic:  
Stankovych, Yevhen Federovych

4. **What is the cardinality of the field "date?"**  
Cardinality of the field "date": single

5. **What would be the correctly formatted value for the field "Host Location" for an item held by an institution in Lviv, the capital of Ukraine's Lviv Oblast?**  
Lviv (Q36036)  
(Copied from Wikidata)

6. **If you wanted to indicate that you were working on a row in our metadata spreadsheet, how would you do that?**  
We would need to type our name in "Claimed by" field in the metadata spreadsheet. 

## Alex's TEI guidelines
1. **What tag should be used to indicate deleted text?**  
`<del>` tag is used to indicate deletions in the text. And then, we need to surround the deleted letter, word, phrase, or lines with `</del>` at the end as well.  
*Example:*  
```xml
<del>I have deleted this text.</del>  
```
URL: <https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#deletions-del>

2. **When should `<damage>` be used instead of `<gap>`?**  
`<damage>` should be used when the text is damaged but can be read with confidence. `<gap>` should be used when the text is completely illegible and cannot be recovered.  
*Example:*
```xml
<p>
The quick brown fox <damage>jumped</damage> over the lazy dog.
</p>
Note: The word 'jumped' is damaged but still readable.

<p>
The quick brown fox <gap reason="illegible" extent="unknown"/> over the lazy dog.
</p>
Note: There's a word missing in the text above that cannot be recovered.
``` 
URL: <https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#uncertain-readings-unclear-gap-damage>

3. **How would you indicate that a word is repeated in the following code block?**
```xml
<p>
The quick brown fox jumped over the the lazy dog.
</p>
```  
When a word or phrase is repeated by accident in the text, add @rend="repeated word" to the `<sic>`. No `<corr>` will be necessary. So, in this case, it should be: 
```xml
<p>
The quick brown fox jumped over the <sic rend="repeated word">the</sic> lazy dog.
</p>

```
URL: <https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#repeated-words>
 
4. **Which tag is used to enclose an entire list of non-book items and which tag is used to enclose a list of books? Which tag should be used to enclose an individual non-book item, and which tag should enclose an individual book item?**  
```xml
List of non-books: <list>
Non-book item: <item>
List of books: <listBibl>
Book items: <bibl> 
```  
*Example:*
```xml
<list>
    <item>Non-book item 1</item>
    <item>Non-book item 2</item>
</list>

<listBibl>
    <head>Book List</head>
    <bibl>Book item 1 details</bibl>
    <bibl>Book item 2 details</bibl>
</listBibl>
```
URL: <https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#lists-structural-markup>


