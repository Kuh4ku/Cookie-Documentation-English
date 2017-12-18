# D2I Files

---

## Introduction

The d2i format is used by Ankama to save the strings from the game for example: item name, dialogues, etc... The file varies from different languages but the structure stays the same.

## The Structure

### _The File_

The file is composed of four major parts:

* The Datas
* The Indexes
* The UI Messages
* some extra data

Each of those parts is composed of an Index \(**4 bytes**\) giving the size of the data that will follow except for the extra data.

### _The Datas_

The datas are composed of three parts:

* Size of all datas \(**4 bytes**\)
* Size of the string \(**2 bytes orange**\)
* The string in UTF-8 \(**X bytes gris**\)

![](/assets/data.PNG)

### _The indexes_

The Indexes since the 2.4X update have become a bit more complicated. The notion of diacritical was introduced \(string without capitals or accents\).

* Size of all the indexes \(**4 bytes**\)
* ID of the string; usually called in the d2o files \(**4 bytes orange**\)
* Diacritical Exists? \(**boolean**\)\(**1 byte light blue **\)
* Pointer to the string \(**4 bytes brown**\)
* If diacritical exists then Pointer to the diacritical string \(**4 bytes dark blue**\)

![](/assets/indexes.PNG)

### _The UI messages_

The UI messages are messages which are given in certain packets that don't use the ID system

**Example:** ui.message.check0

### _Extra data_

At the end of the file there is some extra data which I haven't had time to analyze yet.

### _Schéma_

![](/assets/total.PNG)

### 



