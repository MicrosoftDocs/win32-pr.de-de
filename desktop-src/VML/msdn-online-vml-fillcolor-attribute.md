---
title: VML FillColor-Attribut
description: VML FillColor-Attribut
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339093"
---
# <a name="vml-fillcolor-attribute"></a>VML FillColor-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pinsel Farbe, die den geschlossenen Pfad einer Form füllt. Lese-/Schreibzugriff. [Ivgcolor](msdn-online-vml-ivgcolor.md) .

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* FillColor = " *Expression* " >

**Skript Syntax**

*Element* . FillColor = "*Ausdruck*"

*Ausdruck* = *Element*. FillColor

**Anmerkungen**

Der **FillColor** -Wert wird aus dem **Color** -Attribut des **Fill** -Elements dupliziert.

*VML-Standard Attribut*

**Siehe auch**

[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [ivgcolor](msdn-online-vml-ivgcolor.md)

**Beispiel**

Die Füllfarbe des Rechtecks ist rot.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[FillColor-Attribut Beispiel](/previous-versions/bb229668(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 