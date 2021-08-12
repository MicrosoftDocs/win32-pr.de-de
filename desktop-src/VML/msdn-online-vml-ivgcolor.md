---
title: VML IVgColor
description: VML IVgColor
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97093d9e9315db1389c71db7e8e21fdbf640353c95c5cf11f607c708e1679166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599515"
---
# <a name="vml-ivgcolor"></a>VML IVgColor

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt eine Farbe an.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Eine Zeichenfolge. Textdarstellung der Farbe. Die folgenden benannten Farbtypen werden unterstützt:
<ul>
<li>Schwarz (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Gray (#808080)</li>
<li>Weiß (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rot (#FF0000)</li>
<li>Violett (#800080)</li>
<li>Sollia (#FF00FF)</li>
<li>Grün (#008000)</li>
<li>Limon (#00FF00)</li>
<li>Oliv (#808000)</li>
<li>Gelb (#FFFF00)</li>
<li>Beim (#000080)</li>
<li>Blau (#0000FF)</li>
<li>Teal (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Typ</td>
<td>VgColorType. Typ der Farbe. Einer der folgenden Typen:
<ul>
<li>Mixed</li>
<li>RGB</li>
<li>Schema</li>
<li>benannt</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. RGB-Wert (<strong>Long</strong>) der Farbe. Nur gültig, wenn Type &quot; <strong>RGB</strong> &quot; ist.</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Rote Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Grüne Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Blaue Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
</tbody>
</table>



 

 

 