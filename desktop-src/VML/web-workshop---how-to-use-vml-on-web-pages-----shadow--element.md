---
title: Verwenden des Shadow-Elements
description: Verwenden des Shadow-Elements
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web-Workshop,Shadow-Element
- Entwerfen von Webseiten,Shadow-Element
- Vector Markup Language (VML),Shadow-Element
- VML (Vector Markup Language),Shadow-Element
- Vektorgrafik, Schattenelement
- shadow-Element
- VML-Elemente,Schatten
- VML-Formen, Schattenelement
- Vector Markup Language (VML), Zeichnen mit Schatteneffekten
- VML (Vector Markup Language), Zeichnen mit Schatteneffekten
- Vektorgrafiken,Zeichnen mit Schatteneffekten
- VML-Formen,Zeichnen mit Schatteneffekten
- Zeichnen mit Schatteneffekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512595"
---
# <a name="using-the-shadow-element"></a>Verwenden des Shadow-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie das Unterelement verwendet wird, um eine Form mit `<shadow>` verschiedenen Schatteneffekten zu zeichnen.

Sie können das Unterelement in , oder einem beliebigen vordefinierten Formelement platzieren, um eine `<shadow>` Form mit einem Schatten zu `<shape>` `<shapetype>` zeichnen. Anschließend können Sie die Eigenschaftenattribute des Unterelements verwenden, `<shadow>` um den Schatten anzupassen.

Um beispielsweise eine Form mit einem Schatten zu erstellen, wie in der folgenden Abbildung dargestellt, können Sie die folgenden Zeilen in den Bereich `<BODY>` Ihrer Webseite eingeben:

![shape1.gif (887 Bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` und `type="perspective"` geben an, dass der Schatten mithilfe des Perspektiventyps ein-/aus-en soll.
-   Der **Ursprung und** offset **geben** an, wo der Schatten ge zeichnen werden soll.
-   `matrix="..."` gibt die Perspektivtransformationsmatrix an.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858396)

 

 