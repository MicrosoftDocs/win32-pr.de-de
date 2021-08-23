---
title: VML-StrokeWeight-Attribut
description: VML-StrokeWeight-Attribut
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac5efa964607fdd942c8dff31a4a124d424aa5fbfeede27abc6164fddef087
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680680"
---
# <a name="vml-strokeweight-attribute"></a>VML-StrokeWeight-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Pinselstärke, die den Pfad einer Form strichiert. Lese-/Schreibzugriff. **VGLength**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* strokeweight=" *expression* ">

**Skriptsyntax**

*element* .strokeweight="*expression*"

*expression* = *Element*.strokeweight

**Anmerkungen**

Der Wert wird aus dem **Weight-Attribut** des **Stroke-Elements dupliziert.** Wenn eine Zahl angegeben wird, aber keine Einheiten hinzugefügt werden, ist die Standardeinheit der Emu. Wenn kein Wert angegeben wird, beträgt der Standardwert 1 Pixel (1 px).

Für die Skripterstellung befindet sich die Standardmessungseinheit jedoch in Punkten.

*VML-Standardattribut*

**Siehe auch**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Beispiel**

Die Strichgewichtung der Form beträgt 1 Punkt.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[StrokeWeight-Attribut – Beispiel.](/previous-versions/bb264095(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 