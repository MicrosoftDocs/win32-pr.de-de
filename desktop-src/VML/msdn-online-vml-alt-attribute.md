---
title: VML ALT-Attribut
description: VML ALT-Attribut
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08714efca9a390cbbec2f3dcf14782053d34db3506462214b9e62ebf1da206a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905340"
---
# <a name="vml-alt-attribute"></a>VML ALT-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert alternativen Text, der anstelle einer Grafik angezeigt werden soll. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* alt=" *ausdruck* ">

**Skriptsyntax**

*element* .alt="*expression*"

*expression* = *.alt-Element*

**Anmerkungen**

Das **Alt-Attribut** ähnelt dem STANDARD-HTML-Alt-Attribut.  Dieses Attribut bietet Browsern, die Text in Sprache konvertieren, eine Möglichkeit, grafische Elemente auf einer Seite zu beschreiben.

*VML-Standardattribut*

**Siehe auch**

[Formen](shape-element--vml.md)

**Beispiel**

Das unten stehende **Alt-Element** zeigt den Ausdruck "Rotes Rechteck" in Browsern an, die Webseiten in gesprochene Ausdrücke konvertieren.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Alt-Attribut – Beispiel.](/previous-versions/bb229663(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 