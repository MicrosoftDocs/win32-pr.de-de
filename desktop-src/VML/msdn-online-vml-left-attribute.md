---
title: Linkes VML-Attribut
description: Linkes VML-Attribut
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c067b15281277a85f707f6152fa855c51ee49aba439b16c009f6ff029139a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599288"
---
# <a name="vml-left-attribute"></a>Linkes VML-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt die Position der Form relativ zum linken Element im Dokumentfluss. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="left: *expression* ">

**Skriptsyntax**

*element* .style.left="*expression*"

*expression* = *Element*.style.left

**Anmerkungen**

Das **Left-Attribut** ähnelt dem standardmäßigen HTML **Left-Attribut** für Stile.

Einheiten können dem übergeordneten Element zugeordnet oder in absoluten Einheiten sein. Dieses Attribut wird nicht für Formen geschrieben, die inline verankert sind.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Fluss der Seite.                                                                                                          |
| units      | Eine Zahl mit einem absoluten Einheiten-Designator (cm, mm, in, pt, pc oder px) oder einem relativen Einheiten-Designator (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. |
| Prozentwert | Wert, der als Prozentsatz der Breite des übergeordneten Objekts ausgedrückt wird.                                                                                                    |



 

*VML-Standardattribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Der linke Wert der Form wird im folgenden Beispiel auf 1 festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Left Attribute Example (Beispiel für linkes Attribut).](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 