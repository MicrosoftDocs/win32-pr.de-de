---
title: VML-V-Attribut
description: VML-V-Attribut
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbf2f8654d32714d20e9b0c5a36fb939173698749569692120c04b89e84b6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768330"
---
# <a name="vml-v-attribute"></a>VML-V-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Befehle, die einen Pfad bilden. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* v=" *ausdruck* ">

**Skriptsyntax**

*element* .v="*expression*"

*expression* = *.v-Element*

**Anmerkungen**

Überschreibt das **Path-Attribut** einer Form. Koordinaten können feste Zahlen, relative Zahlen oder Verweise auf Formeln sein (mithilfe des Formats " @n " ", wobei n eine Formelnummer ist, z. B. @2 " " bezieht sich auf die zweite Formel im Formelarray).

*VML-Standardattribut*

**Beispiel**

Ein Rechteck wird  mithilfe des V-Attributs erstellt. Beachten Sie, dass nach dem ersten Satz durch Kommas getrennter Koordinaten ein Kleinbuchstabe L **(lineto-Befehl)** verwendet wird.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 