---
title: Typattribut (Schatten)(VML)
description: Typattribut (Schatten)(VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513160"
---
# <a name="type-attribute-shadowvml"></a>Typattribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den Schattentyp an. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* type="-Ausdruck "> 

**Skriptsyntax**

*element* .type="*expression*"

*expression* = *Element*.type

**Anmerkungen**

Mögliche Werte:



| Wert           | Beschreibung                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | Einzelner Schatten. Standard.                                                                                                                                                                              |
| double          | Ein doppelter Schatten. [Color2](color2-attribute--shadow--vml.md) wird für die Farbe des zweiten Schattens und [Offset2](msdn-online-vml-offset2-attribute.md) für den Offset des zweiten Schattens verwendet. |
| Perspektive     | Ein Perspektivenschatten.                                                                                                                                                                                |
| shapeRelative   | Der Schatten wird relativ zur Form erstellt.                                                                                                                                                         |
| drawingRelative | Der Schatten wird relativ zur Zeichnung erstellt.                                                                                                                                                       |
| Emboss          | Der Schatten hat ein eingebettetes Aussehen.                                                                                                                                                                     |



 

**VML-Standardattribut**

**Beispiel**

Ein doppelter Schatten wird mit dem zweiten Schattengrün und dem Offset 5 Punkte nach unten und rechts erstellt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 