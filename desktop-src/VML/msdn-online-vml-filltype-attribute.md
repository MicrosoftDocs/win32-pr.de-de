---
title: VML FillType-Attribut
description: VML FillType-Attribut
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680800"
---
# <a name="vml-filltype-attribute"></a>VML FillType-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Typ der Füllung, die für den Hintergrund eines Strichs verwendet wird. Lese-/Schreibzugriff. **VgFillType**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* filltype=" *ausdruck* ">

**Skriptsyntax**

*element* .filltype="*expression*"

*expression* = *Element*.filltype

**Anmerkungen**

Mögliche Werte:



| Dashstyle | Beschreibung                                    |
|-----------|------------------------------------------------|
| Basis     | Das Füllmuster ist voll. Standardwert.      |
| Tile      | Das Füllbild ist gekachelt.                       |
| Muster   | Das Füllbild wird gestreckt, um ein Muster zu bilden. |
| Frame     | Das Füllbild wird zu einem Rahmen für die Form. |



 

*VML-Standardattribut*

**Beispiel**

Der Strich der Form verfügt über eine kachelierte Textur, die aus dem cylinder.gif wird.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 