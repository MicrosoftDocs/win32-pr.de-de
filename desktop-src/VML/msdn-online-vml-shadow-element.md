---
title: VML-Schatten Element
description: VML-Schatten Element
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948780"
---
# <a name="vml-shadow-element"></a>VML-Schatten Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Schatten für eine Form.

Die folgenden Attribute ändern einen Schatten.



| Attribut                                          | BESCHREIBUNG                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Farbe](color-attribute--shadow--vml.md)          | Definiert die Farbe eines Schattens.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Definiert die zweite Farbe eines Schattens.              |
| [ID](id-attribute--shadow--vml.md)                | Gibt den eindeutigen Bezeichner eines Schattens an.       |
| [Matrix](matrix-attribute--shadow--vml.md)        | Definiert die perspektivische Transformation eines Schattens.     |
| [Verdeckt](msdn-online-vml-obscured-attribute.md) | Bestimmt, ob der Schatten transparent ist.      |
| [Offset](offset-attribute--shadow--vml.md)        | Definiert, wie weit der Schatten sich hinter der Form erstreckt. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Definiert einen zweiten Offset.                           |
| [Ein](on-attribute--shadow--vml.md)                | Bestimmt, ob ein Schatten angezeigt wird.          |
| [Deckkraft](opacity-attribute--shadow--vml.md)      | Bestimmt die Transparenz eines Schattens.           |
| [Ursprung](origin-attribute--shadow--vml.md)        | Definiert den Mittelpunkt des Schattens.                  |
| [Type](type-attribute--shadow--vml.md)            | Gibt den Typ des Schattens an.                      |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Außerdem muss das [on](on-attribute--shadow--vml.md) -Attribut auf **true** festgelegt werden.

Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Schattens erforderlich ist.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Sie können den Schatten nicht bemerken, es sei denn, Sie erhöhen die [Offset](offset-attribute--shadow--vml.md) Werte, da der Standard Offset 2pt, 2pt ist.

**Beispiele**

-   [Beispiel für einfaches Schatten](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Beispiel für dynamisches Schatten](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 