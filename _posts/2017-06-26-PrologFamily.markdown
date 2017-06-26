---
layout: post
title: Family Relations + PROLOG = ?
---

<img src="/images/fulls/family.jpg" class="fit image">

This time, we explored a little bit in the area of **logical programming**. You may think that this is not very related to AI, but as a matter of fact, it kinda is. AI is, after all, nothing but logical actions programmed to solve a particular problem normally solved by humans.

What we worked on was family relations (a small portion of The Simpsons TV show), modeled with PROLOG. By doing this modeling, we can see a bit of how it can be used: We can ask our model, for example, if two people have a certain relation with each other. Then, PROLOG will answer with a simple boolean: true or false. That's all there is to it, but you can quickly see that PROLOG has a pretty good potential for modeling and solving more complex problems, even AI related problems. It was related to AI after all, don't you agree?

Doing family relations is very simple. First, we had to declare the people on our "world". We did so like this:

```pl
hombre(homero).
hombre(bart).
mujer(lisa).
mujer(marge).
```

Next, we started doing some basic relationships. Things like who are married and who are who's suns.

```
son_esposos(homero,marge).
hijo(homero,bart).
```

And finaly, we made the rules for the rest of the relationships, such as `is_gradpha` and `are_brothers`

```
es_hermano(X,Y):- hijo(Z,X), hijo(Z,Y), hombre(X).
es_abuelo(X,Y):- hijo(X,Z), hijo(Z,Y), hombre(X).
```


[You can see the rest of our code on GitHub!](https://github.com/AI-DreamTeam/p3-prolog/blob/master/Relaciones_Familiares.pl) Happy Hacking! 



