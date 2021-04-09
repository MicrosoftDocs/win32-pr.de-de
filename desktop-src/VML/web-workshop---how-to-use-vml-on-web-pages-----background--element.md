---
title: Verwenden des Background-Elements
description: Verwenden des Background-Elements
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Webworkshop, Hintergrund Element
- Entwerfen von Webseiten, Background-Element
- Vector Markup Language (VML), Background-Element
- VML (Vector Markup Language), Background-Element
- Vektorgrafiken, Hintergrund Element
- Background-Element
- VML-Elemente, Hintergrund
- VML-Formen, Background-Element
- Vector Markup Language (VML), Anpassen von Hintergründen
- VML (Vector Markup Language), Anpassen von Hintergründen
- Vektorgrafiken, Anpassen von Hintergründen
- VML-Formen, Anpassen von Hintergründen
- Anpassen von Hintergründen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858304"
---
# <a name="using-the-background-element"></a>Verwenden des Background-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie Sie den Hintergrund einer Webseite anpassen können, indem Sie das `<background>` in VML bereitgestellte-Element verwenden.

Wie Sie aus dem Thema " [Verwendung `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) " gelernt haben, können Sie das `<fill>` untergeordnete Element innerhalb des `<shape>` , `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um zu beschreiben, wie die Form ausgefüllt wird.

Entsprechend können Sie das untergeordnete `<fill>` -Element im- `<background>` Element platzieren, um zu beschreiben, wie der Hintergrund einer Webseite ausgefüllt wird. Anschließend können Sie die Eigenschafts Attribute des `<fill>` unter Elements verwenden, um den Fülleffekt anzupassen, z. b. die Füllung des [Farbverlaufs](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), die [Musterfüllung](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)oder die [Bild Füllung](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Wenn Sie z. b. einen Hintergrund mit Farbverlauf zeichnen möchten, können Sie die folgenden Zeilen in den `<BODY>` Bereich der Webseite eingeben:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 