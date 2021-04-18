---
title: VML-Pfad Element
description: VML-Pfad Element
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337849"
---
# <a name="vml-path-element"></a>VML-Pfad Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Pfad für eine Form.

Die folgenden Attribute ändern einen Schatten.



| Attribut                                                        | BESCHREIBUNG                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Bestimmt, ob Pfeilspitzen angezeigt werden.                                |
| [Konnektivität](msdn-online-vml-connectangles-attribute.md)     | Gibt an, wie eine Kurve eine Verbindung mit einem Verbindungspunkt herstellt.                       |
| [Connectlocs](msdn-online-vml-connectlocs-attribute.md)         | Definiert den Speicherort von Verbindungs Punkten auf einem Pfad.                            |
| [Connecttype](msdn-online-vml-connecttype-attribute.md)         | Definiert den Typ des Verbindungs Punkts, der zum Anfügen von Formen an andere Formen verwendet wird. |
| [Extrusionok](msdn-online-vml-extrusionok-attribute.md)         | Bestimmt, ob eine-Extrusion angezeigt wird.                              |
| [Fillok](msdn-online-vml-fillok-attribute.md)                   | Bestimmt, ob eine Füllung angezeigt wird.                                    |
| [Gradientshapeok](msdn-online-vml-gradientshapeok-attribute.md) | Bestimmt, ob eine Form vom Typ "Verlauf" angezeigt wird.                          |
| [ID](id-attribute--path--vml.md)                                | Definiert einen eindeutigen Bezeichner für einen Pfad.                                         |
| [Limo](msdn-online-vml-limo-attribute.md)                       | Definiert einen streckungs Punkt auf dem Pfad.                                            |
| [Shadowok](msdn-online-vml-shadowok-attribute.md)               | Bestimmt, ob ein Schatten angezeigt wird.                                  |
| [Strokeok](msdn-online-vml-strokeok-attribute.md)               | Bestimmt, ob ein Strich angezeigt wird.                                  |
| [Textboxrect](msdn-online-vml-textboxrect-attribute.md)         | Definiert ein oder mehrere Textfelder innerhalb einer Form.                                   |
| [Textpathok](msdn-online-vml-textpathok-attribute.md)           | Bestimmt, ob ein TextPath angezeigt wird.                                |
| [B](msdn-online-vml-v-attribute.md)                             | Definiert die Befehle, die einen Pfad bilden.                                       |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Der folgende Code zeigt, wie eine Form mit einem Pfad definiert wird.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Beachten Sie, dass das Attribut " [V](msdn-online-vml-v-attribute.md) " des **Pfads** das [Pfad](msdn-online-vml-path-attribute.md) Attribut von " [Shape](shape-element--vml.md)" ersetzt

**Beispiele**

-   [Beispiel für ein untergeordnetes Pfad-Element](/previous-versions/bb229545(v=vs.85))
-   [Beispiel für das untergeordnete Dynamic Path](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 