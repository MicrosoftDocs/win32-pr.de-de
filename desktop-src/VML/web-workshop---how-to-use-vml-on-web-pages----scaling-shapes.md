---
title: Skalieren von Formen
description: Skalieren von Formen
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web-Workshop,Skalieren von Formen
- Entwerfen von Webseiten, Skalieren von Formen
- Vector Markup Language (VML), Skalieren von Formen
- VML (Vector Markup Language), Skalieren von Formen
- Vektorgrafiken,Formen skalieren
- VML-Formen,Skalierung
- Skalieren von Formen
- Vector Markup Language (VML), Größen für Formen
- VML (Vector Markup Language), Größen für Formen
- Vektorgrafiken, Größen für Formen
- VML-Formen, Größen
- Anpassen der Größe von Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc7f62d802548ef1bc19aabf33c886c5b826098ae1280a9dd0b69413c9a61aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057013"
---
# <a name="scaling-shapes"></a>Skalieren von Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Sie haben gelernt, wie Sie mithilfe von VML Formen auf einer Webseite zeichnen und färben. In diesem Thema wird veranschaulicht, wie Sie Formen auf eine beliebige Größe skalieren.

VML verwendet die gleiche Syntax, die im Abschnitt Details zum visuellen [Renderingmodell](https://www.w3.org/TR/PR-CSS2/visudet.mdl) der [CSS2-Spezifikation](https://www.w3.org/TR/PR-CSS2/) definiert ist, um die Größe des enthaltenden Felds anzugeben, sodass der Inhalt einer Form innerhalb des enthaltenden Felds gerendert (gezeichnet) wird. Sie können die **Breiten- und** **Höhenstilattribute** verwenden, um die Größe des enthaltenden Felds zu definieren.

Wenn Sie beispielsweise ein Oval zeichnen und style ='width:75pt;height:100pt' angeben, wird das Oval in einem enthaltenden Feld mit einer Größe von 75 Punkten (Breite) um 100 Punkte (Höhe) gezeichnet, wie in der folgenden Abbildung gezeigt:

![oval1.gif (660 Bytes)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Wenn Sie die Größe in style ='width:120pt;height:140pt' ändern, wird das Oval größer, da es innerhalb des neuen enthaltenden Felds mit einer Größe von 120 Punkten (Breite) um 140 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung gezeigt:

![oval2.gif (966 Bytes)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Wenn Sie die Größe in style ='width:60pt;height:40pt' ändern, wird das Oval kleiner, da es innerhalb des neuen enthaltenden Felds mit einer Größe von 60 Punkten (Breite) um 40 Punkte (Höhe) skaliert wird, wie in der folgenden Abbildung gezeigt:

![oval3.gif (394 Bytes)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 