---
title: Verwenden des Shadow-Elements
description: Verwenden des Shadow-Elements
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Webworkshop, Schatten Element
- Entwerfen von Webseiten, Schatten Element
- Vector Markup Language (VML), Schatten Element
- VML (Vector Markup Language), Schatten Element
- Vektorgrafiken, Schatten Element
- Shadow-Element
- VML-Elemente, Schatten
- VML-Formen, Schatten Element
- Vector Markup Language (VML), zeichnen mit Schatteneffekten
- VML (Vector Markup Language), zeichnen mit Schatteneffekten
- Vektorgrafiken, zeichnen mit Schatteneffekten
- VML-Formen, zeichnen mit Schatteneffekten
- Zeichnen mit Schatteneffekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390918"
---
# <a name="using-the-shadow-element"></a>Verwenden des Shadow-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie Sie mit dem `<shadow>` untergeordneten Element eine Form mit verschiedenen Schatteneffekten zeichnen.

Sie können das `<shadow>` untergeordnete Element in `<shape>` , oder einem `<shapetype>` beliebigen vordefinierten Shape-Element platzieren, um eine Form mit einem Schatten zu zeichnen. Sie können dann die Eigenschafts Attribute des `<shadow>` unter Elements verwenden, um den Schatten anzupassen.

Wenn Sie z. b. eine Form mit einem Schatten erstellen möchten, wie in der folgenden Abbildung gezeigt, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` und `type="perspective"` geben an, dass der Schatten mit dem Perspective-Typ aktiviert werden soll.
-   Der **Ursprung** und der **Offset** geben an, wo der Schatten gezeichnet werden soll.
-   `matrix="..."` Gibt die Perspektiven Transformationsmatrix an.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 