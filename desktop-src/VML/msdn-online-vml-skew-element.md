---
title: VML-Schiefe-Element
description: VML-Schiefe-Element
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e317d03fc0bbef361df56282bec55ea2a9e708f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473156"
---
# <a name="vml-skew-element"></a>VML-Schiefe-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine schiefe für eine Form.

Die folgenden Attribute ändern eine schiefe.



| Attribut                                 | BESCHREIBUNG                                    |
|-------------------------------------------|------------------------------------------------|
| [Antrags](ext-attribute--skew--vml.md)       | Definiert die Art und Weise, wie eine schiefe angezeigt wird.           |
| [ID](id-attribute--skew--vml.md)         | Definiert einen eindeutigen Bezeichner für eine schiefe.        |
| [Matrix](matrix-attribute--skew--vml.md) | Definiert eine perspektivische Transformation für eine schiefe.    |
| [Offset](offset-attribute--skew--vml.md) | Definiert den Offset einer Schiefe.                  |
| [Ein](on-attribute--skew--vml.md)         | Bestimmt, ob die Schiefe angezeigt wird. |
| [Ursprung](origin-attribute--skew--vml.md) | Bestimmt den Ursprung einer Schiefe.               |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Außerdem müssen die Attribute [Matrix](matrix-attribute--skew--vml.md) und [on](on-attribute--skew--vml.md) auf **true** festgelegt werden.

Im folgenden finden Sie den minimalen Code, der zum verursachen einer Schiefe erforderlich ist.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



Das **schiedeelement** ist eine Microsoft Office Erweiterung von VML.

**Beispiele**

-   [Beispiel für eine einfache Schiefe](/previous-versions/bb229482(v=vs.85))
-   [Beispiel für dynamische Schiefe](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 