---
title: VML-Höhenattribut
description: VML-Höhenattribut
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49218b83834d0d276d458656376d1806089be00a2158f271e38a4ee8da8099c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136993"
---
# <a name="vml-height-attribute"></a>VML-Höhenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt die Höhe der Form an. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="height: *ausdruck* ">

**Skriptsyntax**

*element* .style.height="*expression*"

*expression* = *Element*.style.height

**Anmerkungen**

Das **Height-Attribut** ähnelt dem HTML **Height-Standardattribut** für Stile.

Einheiten können dem übergeordneten Element zugeordnet oder in absoluten Einheiten sein.

Mögliche Werte:



| Wert      | Beschreibung                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Fluss der Seite.                                                                                                          |
| units      | Eine Zahl mit einem absoluten Einheiten-Designator (cm, mm, in, pt, pc oder px) oder einem relativen Einheiten-Designator (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. |
| Prozentwert | Wert, der als Prozentsatz der Höhe des übergeordneten Objekts ausgedrückt wird.                                                                                                   |



 

*VML-Standardattribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Die Höhe der Form ist auf 30 festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Height-Attribut – Beispiel.](/previous-versions/bb229671(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 