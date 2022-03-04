---
layout: page
title: 'Book Search Guide: Pounce/Pounce+ and UofM Campuses Databases'
toc: true
toc_title: Contents
---

<style>
    .hide{
    display: none;
}
</style>

# Searching for Materials in Pounce and in Cross-Campus Databases
This guide will first layout the key points of using an advanced search to find materials within [our database](https://primo.lib.umn.edu/primo-explore/search?vid=MORRIS&lang=en_US&sortby=rank&tab=default_tab), and then provide a template of sample
questions and how you would translate them into search conditions.  

## Advanced Search: Overview of Search Filters  
### Common Search Categories  
In the [advanced search tab](https://primo.lib.umn.edu/primo-explore/search?vid=MORRIS&lang=en_US&sortby=rank&tab=default_tab&mode=advanced), the first box contains categories which narrow down the fields in which given keywords will be looked for.  
- **Any field**: The default search, this works like a broad keyword search that will look for any instance of the keyword within any of the other categories.
- **Title**: Look for books by their title/words contained within the title.
- **Author/creator**: Look for books by the author's name.
- **Subject**: Look for books by associated subject.
- **ISBN**: Look for a book by its International Standard Book Number.
- **ISSN**: Search for a book by its International Standard Serial Number.
- **Creation Date**: Search for books created on the given date.  

### Search Parameters  
The second box contains search parameters. Parameters will decide how keywords will be looked for within a given category.  
- **Contains**: How you might normally think of a keyword search, this parameter searches for any instance of the keywords. This will be the default, which you will use most of the time.
- **Is (exact)**: This parameter will only find things that exactly match the given keywords within a selected category.
- **Starts with**: This parameter will find anything that starts with the given keywords within a selected category.  

### Collections
In the top right of the advanced search tab, you will see a dropdown box labeled **Collection**. This allows you to choose the type of materials you will be looking for, almost like different categories.

For example, choosing the DVDs collection will give you back results for, you guessed it, DVDs.


## Translating Questions Into Search Parameters  
Following are example templates of questions you might hear from a patron and how you should connect them to a book search.  
### "Do you have this book by this author?"  
Here you will search using both tile and author name. Most of the time, book titles will be different from how they are normally called, so it is easier
when you aren't certain you have the exact title to use the default **contains** search parameter.  

### "Do you have a book about this?"  
Here you will search using the Subject category.  

### "Do you have any books by this author?"  
A simple Author/creator search.  

### "I can't remember the title, but it was about this..."  
Here you might think to do a general keyword search, but it would be more helpful to search by subject and keyword both.  

## Search Practice
Now that you've seen how the advanced search is set up and some common types of searches, try finding the books below through advanced search for Pounce/Pounce+ and UofM Campuses using different categories and parameters. When finding the books, take note of things such as how many results appear, whether the book appears on one database but not another, and how more specific keywords narrows down searches.

<div id='start'>Searching by author J.R.R Tolkien, find the first book in the Lord of the Rings trilogy, The Fellowship of the Ring.</div>
<button onclick="show('next1')">Next Book</button>
<div id='next1' class="hide">
    <br />Using a keyword search with at most two keywords, find the book "China and the West: Music, Representation, and Reception".<br />
    <button onclick="show('next2')">Next Book</button>
    <div id='next2' class="hide">
        <br />Find a book related to rhetoric that was created in 1978 and has been published by the Cornell University Press.
    </div>
</div>

## Next try out the [Book Search Quiz](quiz.md)

<script>
function show(id) {
    var myDiv = document.getElementById(id);
    myDiv.classList.toggle("hide");
}
</script>
