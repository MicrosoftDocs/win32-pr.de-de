---
title: VML Path-Element
description: VML Path-Element
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb46ce43d2dc9ad80aeb21340dceacde80feba99d9debdf66920b662eeaf3a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308180"
---
# <a name="vml-path-element"></a>VML Path-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen Pfad für eine Form.

Die folgenden Attribute ändern einen Schatten.



| attribute                                                        | BESCHREIBUNG                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Bestimmt, ob Pfeilspitzen angezeigt werden.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Gibt an, wie eine Kurve eine Verbindung mit einem Verbindungspunkt herstellt.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Definiert den Speicherort von Verbindungspunkten in einem Pfad.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Definiert den Typ des Verbindungspunkts, der zum Anfügen von Formen an andere Formen verwendet wird. |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | Bestimmt, ob eineExtrusion angezeigt wird.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Bestimmt, ob eine Füllung angezeigt wird.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Bestimmt, ob eine Farbverlaufsform angezeigt wird.                          |
| [ID](id-attribute--path--vml.md)                                | Definiert einen eindeutigen Bezeichner für einen Pfad.                                         |
| [Limo](msdn-online-vml-limo-attribute.md)                       | Definiert einen Stretchpunkt auf dem Pfad.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Bestimmt, ob ein Schatten angezeigt wird.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Bestimmt, ob ein Strich angezeigt wird.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Definiert ein oder mehrere Textfelder innerhalb einer Form.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Bestimmt, ob ein Textpfad angezeigt wird.                                |
| [B](msdn-online-vml-v-attribute.md)                             | Definiert die Befehle, die einen Pfad bilden.                                       |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements](shape-element--vml.md) definiert werden.

Der folgende Code zeigt, wie eine Form mit einem Pfad definiert wird.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Beachten Sie, dass das [V-Attribut](msdn-online-vml-v-attribute.md) von **Path** das [Path-Attribut](msdn-online-vml-path-attribute.md) von [Shape](shape-element--vml.md)ersetzt.

**Beispiele**

-   [Beispiel für untergeordnetes Element des einfachen Pfads](/previous-versions/bb229545(v=vs.85))
-   [Beispiel für untergeordnetes Element des dynamischen Pfads](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 