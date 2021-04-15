---
title: Verwenden des TextBox-Elements
description: Verwenden des TextBox-Elements
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Webworkshop, TextBox-Element
- Entwerfen von Webseiten, TextBox-Element
- Vector Markup Language (VML), TextBox-Element
- VML (Vector Markup Language), TextBox-Element
- Vektorgrafiken, TextBox-Element
- Textfeld-Element
- VML-Elemente, TextBox
- VML-Formen, TextBox-Element
- Vector Markup Language (VML), Anfügen von Text
- VML (Vector Markup Language), Anfügen von Text
- Vektorgrafiken, Anfügen von Text
- VML-Formen, Anfügen von Text
- Anfügen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474124"
---
# <a name="using-the-textbox-element"></a>Verwenden des TextBox-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Beispiele:

Um Text an ein Rechteck anzufügen, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Um einen Hyperlink an ein abgerundetes Rechteck anzufügen, das mit einem Farbverlauf gefüllt ist, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:

![textbox2.gif (1147 Bytes)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 