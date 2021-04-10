---
title: VML-textboxrect-Attribut
description: VML-textboxrect-Attribut
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039058"
---
# <a name="vml-textboxrect-attribute"></a>VML-textboxrect-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert ein oder mehrere Textfelder innerhalb einer Form. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Pfad](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *Element* textboxrect = " *Expression* " >

**Skript Syntax**

*Element* . textboxrect = "*Ausdruck*"

*Ausdruck* = *Element*. textboxrect

**Anmerkungen**

Ein Textfeld wird durch mindestens einen Satz von Zahlen definiert, der (in der Reihenfolge) die linken, oberen, rechten und unteren Punkte des Rechtecks angibt. Mehrere Sätze werden durch ein Semikolon getrennt. Der Standardwert ist derselbe Dimensions Wert wie das enthaltende Rechteck. Wenn mehr als ein Textfeld definiert ist, werden die durch Trennzeichen getrennten viertsets, die jedes Textfeld definieren, durch Semikolons getrennt. Normalerweise treten Textfelder in Sätzen von 1, 2, 3 oder 6 Rechtecke in einer Form auf.

*VML-Standard Attribut*

**Beispiel**

In der linken oberen Ecke der Form wird ein text95 Feld mit einer Einheit von 95 Einheiten definiert und 5 Einheiten platziert.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 