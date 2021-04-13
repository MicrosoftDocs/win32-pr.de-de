---
title: Position-Attribut (Form) (VML)
description: Position-Attribut (Form) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390966"
---
# <a name="position-attribute-shapevml"></a>Position-Attribut (Form) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Positionstyp, der zum Platzieren eines Elements verwendet wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "Position: *Ausdruck* " >

**Skript Syntax**

*Element* . Style. Position = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Position

**Anmerkungen**

Das **Positions** Attribut ähnelt dem standardmäßigen HTML- **Positions** Attribut, das mit Stylesheets verwendet wird.

Mögliche Werte:



| Wert    | BESCHREIBUNG                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Standard. Das-Element wird gemäß dem normalen Fluss der Seite positioniert. Die Attribute **Top** und **left** werden ignoriert. Wenn das Objekt Inline verankert ist, was nur in Microsoft Word geschieht, wird dieser Wert verwendet. |
| absolute | Das-Element wird relativ zum übergeordneten Element positioniert, wobei die Attribute **Top** und **left** verwendet werden. Dieser Wert wird von den Gleit Komma Objekten Microsoft Word und Microsoft Excel sowie von Microsoft PowerPoint-Folien verwendet.                  |
| relative | Das-Element wird gemäß dem normalen Ablauf der Seite positioniert, aber die Attribute **Top** und **left** werden verwendet. Die Überlappung der überlappenden Elemente wird durch das **Z-Index-** Attribut geregelt.                       |



 

*VML-Standard Attribut*

**Beispiel**

Die Position des Rechtecks wird mit dem *relativen* Stil angezeigt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel für das Positions Attribut](/previous-versions/bb264090(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 