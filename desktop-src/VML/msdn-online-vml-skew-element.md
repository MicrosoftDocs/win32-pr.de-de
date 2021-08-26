---
title: VML-Skew-Element
description: VML-Skew-Element
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099040"
---
# <a name="vml-skew-element"></a>VML-Skew-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Schiefe für eine Form.

Die folgenden Attribute ändern eine Schiefe.



| attribute                                 | BESCHREIBUNG                                    |
|-------------------------------------------|------------------------------------------------|
| [Extern](ext-attribute--skew--vml.md)       | Definiert, wie eine Schiefe angezeigt wird.           |
| [ID](id-attribute--skew--vml.md)         | Definiert einen eindeutigen Bezeichner für eine Schiefe.        |
| [Matrix](matrix-attribute--skew--vml.md) | Definiert eine Perspektiventransformation für eine Schiefe.    |
| [Offset](offset-attribute--skew--vml.md) | Definiert den Offset einer Schiefe.                  |
| [Ein](on-attribute--skew--vml.md)         | Bestimmt, ob die Schiefe angezeigt wird. |
| [Ursprung](origin-attribute--skew--vml.md) | Bestimmt den Ursprung einer Schiefe.               |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements](shape-element--vml.md) definiert werden.

Darüber hinaus müssen die Attribute [Matrix](matrix-attribute--skew--vml.md) und [On](on-attribute--skew--vml.md) auf **True** festgelegt werden.

Im Folgenden ist der mindest erforderliche Code zum Erzeugen einer Schiefe.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



Das **Skew-Element** ist eine Microsoft Office-Erweiterung für VML.

**Beispiele**

-   [Beispiel für einfache Schiefe](/previous-versions/bb229482(v=vs.85))
-   [Beispiel für dynamische Schiefe](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 