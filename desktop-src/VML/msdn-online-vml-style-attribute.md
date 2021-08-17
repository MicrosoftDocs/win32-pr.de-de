---
title: VML-Formatattribut
description: VML-Formatattribut
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475190"
---
# <a name="vml-style-attribute"></a>VML-Formatattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Stil des Frames. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *element* style="-Ausdruck "> 

**Skriptsyntax**

*element* .style="*expression*"

*expression* = *.style-Element*

**Anmerkungen**

Dieses Attribut verwendet die normalen CSS-Stilattribute für die Positionierung.

*VML-Standardattribut*

**Beispiel**

Der Stil definiert die tatsächliche Position des Frames.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 