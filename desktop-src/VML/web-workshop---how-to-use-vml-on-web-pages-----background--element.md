---
title: Verwenden des Background-Elements
description: Verwenden des Background-Elements
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web workshop,background-Element
- Entwerfen von Webseiten, Hintergrundelement
- Vector Markup Language (VML),Hintergrundelement
- VML (Vector Markup Language),Background-Element
- Vektorgrafiken, Hintergrundelement
- background-Element
- VML-Elemente, Hintergrund
- VML-Formen, Hintergrundelement
- Vector Markup Language (VML), Anpassen von Hintergründen
- VML (Vector Markup Language),Anpassen von Hintergründen
- Vektorgrafiken, Anpassen von Hintergründen
- VML-Formen, Anpassen von Hintergründen
- Anpassen von Hintergründen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512780"
---
# <a name="using-the-background-element"></a>Verwenden des Background-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie Sie den Hintergrund einer Webseite mithilfe des `<background>` in VML bereitgestellten Elements anpassen können.

Wie Sie aus dem [ `<fill>` Thema Verwenden](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) gelernt haben, können Sie das `<fill>` Unterelement in , `<shape>` oder `<shapetype>` einem beliebigen vordefinierten Shape-Element platzieren, um zu beschreiben, wie die Form gefüllt wird.

Auf ähnliche Weise können Sie das Unterelement innerhalb des -Elements platzieren, `<fill>` `<background>` um zu beschreiben, wie der Hintergrund einer Webseite ausgefüllt wird. Anschließend können Sie die Eigenschaftenattribute des `<fill>` Unterelements verwenden, um den Fülleffekt anzupassen, z. B. [Farbverlaufsfüllung,](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) [Musterfüllung](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)oder [Bildfüllung.](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)

Um z. B. einen mit Farbverlauf gefüllten Hintergrund zu zeichnen, können Sie die folgenden Zeilen im `<BODY>` Bereich Ihrer Webseite eingeben:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858389)

 

 