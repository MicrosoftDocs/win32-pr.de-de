---
title: Aufgefülltes VML-Attribut
description: Aufgefülltes VML-Attribut
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7053263f989dbbef163e04ca19e28afa882d20347b103c97cf2db3be4b8d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346604"
---
# <a name="vml-filled-attribute"></a>Aufgefülltes VML-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob der geschlossene Pfad ausgefüllt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* filled=" *ausdruck* ">

**Skriptsyntax**

*element* .filled="*expression*"

*expression* = *element*.filled

**Anmerkungen**

Der Wert wird aus dem **On-Attribut** des [Fill-Elements](msdn-online-vml-fill-element.md) dupliziert.

*VML-Standardattribut*

**Beispiel**

Der Formpfad ist gefüllt.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für ein gefülltes Attribut.](/previous-versions/bb229669(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 