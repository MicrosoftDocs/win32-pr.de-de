---
title: Color2-Attribut (Stroke)(VML)
description: Color2-Attribut (Stroke)(VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108c767f7337f486f8b7df5a4506b3b3d487dabf146656890def0c5e1ad32a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867430"
---
# <a name="color2-attribute-strokevml"></a>Color2-Attribut (Stroke)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine zweite Farbe für Striche. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* color2="-Ausdruck "> 

Skriptsyntax

*element* .color2="*expression*"

*expression* = *Element*.color2

**Anmerkungen**

Eine zweite Farbe wird verwendet, wenn der Fülltyp eines Strichs ein Muster ist.

*VML-Standardattribut*

**Beispiel**

Der Strich der Form ist eine Musterfüllung, bei der die Füllung durch das Quellbild definiert wird, der transparente Hintergrund jedoch durch die zweite Farbe definiert wird.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 