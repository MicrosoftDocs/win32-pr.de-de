---
title: VML FocusSize-Attribut
description: VML FocusSize-Attribut
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322bea9f9d78ff76cd631cc36149939bb5b3db5f87dc9c80e9f2a5100f031c1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099260"
---
# <a name="vml-focussize-attribute"></a>VML FocusSize-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Fokusgröße für radiale Füllungen. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* focussize="-Ausdruck "> 

**Skriptsyntax**

*element* .focussize="*expression*"

*expression* = *Element*.focussize

**Anmerkungen**

Die Werte sind Bruchteile der Breite und Höhe der Form. Die erste ist ein Prozentsatz der Füllung am rechten Rand der Form, und die zweite ist ein Prozentsatz der Füllung am unteren Rand der Form. Der Standardwert ist 0,0. Ein **FocusSize-Wert** von 100 %,100 % und eine **FocusPosition** von 0,0 würden dazu sorgen, dass Color2 die Mischung vollständig überträgt. Für ausgewogene Mischungen werden kleine Werte von etwa 10 %,10 % empfohlen.

*VML-Standardattribut*

**Beispiel**

Die radiale Füllung erstellt eine Mischung, die in der Mitte blau beginnt und an allen vier Rändern rot wird. Der Mittelpunkt der Mischung wird durch **FocusPosition definiert,** und die Größe der inneren Anfangsfarbe wird durch **FocusSize bestimmt.**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 