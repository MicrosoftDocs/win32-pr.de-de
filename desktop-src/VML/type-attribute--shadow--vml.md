---
title: Type-Attribut (Schatten) (VML)
description: Type-Attribut (Schatten) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390665"
---
# <a name="type-attribute-shadowvml"></a>Type-Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den Typ des Schattens an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Elementtyp* = " *Ausdruck* " >

**Skript Syntax**

*Element* . Type = "*Ausdruck*"

*Ausdruck* = *Element*. Type

**Anmerkungen**

Mögliche Werte:



| Wert           | BESCHREIBUNG                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | Einzelner Schatten. Standard.                                                                                                                                                                              |
| double          | Ein doppelter Schatten. [Color2](color2-attribute--shadow--vml.md) wird für die Farbe des zweiten Schattens verwendet, und [Offset2](msdn-online-vml-offset2-attribute.md) wird für den Offset des zweiten Schattens verwendet. |
| Perspektive     | Ein Perspektiven Schatten.                                                                                                                                                                                |
| shaperelative   | Der Schatten wird relativ zur Form erstellt.                                                                                                                                                         |
| drawingrelative | Der Schatten wird relativ zum Zeichnen erstellt.                                                                                                                                                       |
| Prägung          | Der Schatten hat ein geprägte aussehen.                                                                                                                                                                     |



 

**VML-Standard Attribut**

**Beispiel**

Ein doppelter Schatten wird mit dem zweiten Schatten grün und Offset 5 nach unten und nach rechts erstellt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 