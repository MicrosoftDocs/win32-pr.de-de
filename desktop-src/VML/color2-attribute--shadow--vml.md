---
title: Color2-Attribut (Schatten)(VML)
description: Color2-Attribut (Schatten)(VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241c7e0a620b6b5f2f54a8849779dcc905d027781fe38a5121ca74b6acbeac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655700"
---
# <a name="color2-attribute-shadowvml"></a>Color2-Attribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die zweite Farbe eines Schattens. Lese-/Schreibzugriff. **VgColor**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* color2="-Ausdruck "> 

**Skriptsyntax**

*element* .color2="*expression*"

*expression* = *Element*.color2

**Anmerkungen**

Verwenden Sie eine zweite Farbe, um spezielle Schatteneffekte zu erstellen. Weitere Informationen [zu zweiten](type-attribute--shadow--vml.md) Farben finden Sie unter Type-Attribut.

*VML-Standardattribut*

**Beispiel**

Der Schatten hat blau für eine zweite Farbe.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 