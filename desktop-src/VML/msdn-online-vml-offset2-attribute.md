---
title: VML Offset2-Attribut
description: VML Offset2-Attribut
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc06b68f075b139f6822a38672b8530fc2172071aab35072659968725d9866b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124223"
---
# <a name="vml-offset2-attribute"></a>VML Offset2-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt einen zweiten Offset. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* offset2="-Ausdruck "> 

**Skriptsyntax**

*element* .offset2="*expression*"

*expression* = *Element*.offset2

**Anmerkungen**

Der Standardwert für einen zweiten Offset für den x-Wert ist 0, und der Standardwert für den y-Wert ist 0. Werte sind entweder eine absolute Messung oder ein Bruchwert der Form. Bei Bruchwerten liegen die Werte zwischen 50 % und -50 %.

Verwenden Sie einen zweiten Offset, um spezielle Schatteneffekte zu erstellen. Weitere Informationen [zu zweiten](type-attribute--shadow--vml.md) Offsets finden Sie unter Type-Attribut.

*VML-Standardattribut*

**Beispiel**

Für die Form wird ein doppelter Schatten erstellt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 