---
title: Src-Attribut (Stroke)(VML)
description: Src-Attribut (Stroke)(VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bc71d7a36ee944a2352cde6bfa1ef33f0b5c480d78c7aada751ea67db9ca7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596626"
---
# <a name="src-attribute-strokevml"></a>Src-Attribut (Stroke)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert das Quellbild, das für eine Strichfüllung geladen werden soll. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* src=" *ausdruck* ">

**Skriptsyntax**

*element* .src="*expression*"

*expression* = *.src-Element*

**Anmerkungen**

URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten verweisen, damit ein Bild angezeigt wird. Wenn dieses Attribut allein angezeigt wird, d. h. keine **HRef-** oder **Title-Eigenschaft,** wird das Bild verknüpft.

*VML-Standardattribut*

**Beispiel**

Der Strich wird mit dem von der cylinder.gif-Datei angegebenen Bild erstellt.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 