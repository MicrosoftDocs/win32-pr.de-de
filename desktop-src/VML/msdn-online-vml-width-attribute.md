---
title: VML-Breitenattribut
description: VML-Breitenattribut
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385aee5c45f68d039bc1bcf6bd3b0c52db0871640bc8a2df3a7f25e9e2bdc205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938957"
---
# <a name="vml-width-attribute"></a>VML-Breitenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Breite der Form. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="width: *expression* ">

**Skriptsyntax**

*element* .style.width="*expression*"

*expression* = *Element*.style.width

**Anmerkungen**

Das **Width-Attribut** ähnelt dem **Html-Standardbreitenattribut** für Stile.

Einheiten können dem übergeordneten Element zugeordnet oder in absoluten Einheiten sein.

Mögliche Werte:



| Wert      | Beschreibung                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Seitenfluss.                                                                                                          |
| units      | Eine Zahl mit einem absoluten Einheiten-Kennzeichner (cm, mm, in, pt, pc oder px) oder einem bezeichner für relative Einheiten (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. |
| Prozentwert | Der Als Prozentsatz der Breite des übergeordneten Objekts ausgedrückte Wert.                                                                                                    |



 

*VML-Standardattribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Die Breite der Form ist 25.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Width-Attribut – Beispiel.](/previous-versions/bb264101(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 