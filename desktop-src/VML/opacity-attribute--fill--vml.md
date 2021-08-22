---
title: Opacity-Attribut (Fill)(VML)
description: Opacity-Attribut (Fill)(VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ea4f539eb2386dae7b8e863c95556cf70400c320ee515897cf7f96a85fe3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057598"
---
# <a name="opacity-attribute-fillvml"></a>Opacity-Attribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Transparenz einer Füllung. Lese-/Schreibzugriff. [VgFraction](msdn-online-vml-vgfraction-data-type.md).

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* opacity=" *ausdruck* ">

**Skriptsyntax**

*element* .opacity="*expression*"

*expression* = *.opacity-Element*

**Anmerkungen**

Der Standardwert ist 1,0.

*VML-Standardattribut*

**Beispiel**

Die Füllung der Form ist zu 50 % transparent.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 