---
title: Verwenden des Textbox-Elements
description: Verwenden des Textbox-Elements
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web-Workshop,Textbox-Element
- Entwerfen von Webseiten,Textbox-Element
- Vector Markup Language (VML),textbox-Element
- VML (Vector Markup Language),textbox-Element
- Vektorgrafik,Textbox-Element
- textbox-Element
- VML-Elemente, Textfeld
- VML-Formen, Textfeldelement
- Vector Markup Language (VML), Anfügen von Text
- VML (Vector Markup Language),Anfügen von Text
- Vektorgrafiken,Anfügen von Text
- VML-Formen,Anfügen von Text
- Anfügen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a9b4cb0b9096777a017dafd7df1c738621a4d5681ac3228741b3fd30386ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512625"
---
# <a name="using-the-textbox-element"></a>Verwenden des Textbox-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

## <a name="examples"></a>Beispiele:

Zum Anfügen von Text an ein Rechteck können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Um einen Link an ein abgerundetes Rechteck mit Farbverlaufsfüllung anfügen zu können, können Sie die folgenden Zeilen in den Bereich `<BODY>` der Webseite eingeben:

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





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858397)

 

 