---
title: Skalieren von Formen
description: Skalieren von Formen
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Webworkshop, Skalieren von Formen
- Entwerfen von Webseiten, Skalieren von Formen
- Vector Markup Language (VML), Skalieren von Formen
- VML (Vector Markup Language), Skalieren von Formen
- Vektorgrafiken, Skalierungs Formen
- VML-Formen, Skalierung
- Skalieren von Formen
- Vector Markup Language (VML), Größen Anpassungs Formen
- VML (Vector Markup Language), Größen Anpassungs Formen
- Vektorgrafiken, Größen Anpassungs Formen
- VML-Formen, Größenanpassung
- Größen Anpassungs Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727937"
---
# <a name="scaling-shapes"></a>Skalieren von Formen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Sie haben gelernt, wie Formen mithilfe von VML auf einer Webseite gezeichnet werden können. In diesem Thema wird veranschaulicht, wie Sie Formen auf eine beliebige Größe skalieren.

VML verwendet dieselbe Syntax, die im Abschnitt " [Details zum visuellen Renderingmodell](https://www.w3.org/TR/PR-CSS2/visudet.mdl) " der "CSS2"- [Spezifikation](https://www.w3.org/TR/PR-CSS2/) definiert ist, um die Größe des enthaltenden Felds anzugeben, damit der Inhalt einer Form im enthaltenden Feld gerendert wird. Mit den Attributen **Width** und **height** können Sie die Größe des enthaltenden Felds definieren.

Wenn Sie z. b. ein Oval zeichnen und **Style**= ' width: 75pt; height: 100pt ' angeben, wird das Oval innerhalb eines enthaltenden Felds mit einer Größe von 75 Punkten (Breite) um 100 Punkte (Höhe) gezeichnet, wie in der folgenden Abbildung dargestellt:

![oval1.gif (660 bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Wenn Sie die Größe in **Style**= "width: 120pt; height: 140pt" ändern, wird das Oval größer, da es im neuen enthaltenden Feld mit einer Größe von 120 Punkten (Breite) um 140 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung dargestellt:

![oval2.gif (966 bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Wenn Sie die Größe in **Style**= "width: 60pt; height: 40 PT" ändern, wird das Oval kleiner, da es im neuen enthaltenden Feld mit einer Größe von 60 Punkten (Breite) um 40 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung dargestellt:

![oval3.gif (394 bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 