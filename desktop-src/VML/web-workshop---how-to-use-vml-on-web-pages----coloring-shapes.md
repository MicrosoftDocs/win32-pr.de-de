---
title: Färben von Formen
description: In diesem Artikel wird das Färben von Formen in VML beschrieben, ein Feature, das ab Version Windows Internet Explorer 9 veraltet ist.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web-Workshop,Färben von Formen
- Entwerfen von Webseiten, Färben von Formen
- Vector Markup Language (VML), färbende Formen
- VML (Vector Markup Language),färbende Formen
- Vektorgrafiken, färbende Formen
- VML-Formen, Färbung
- Färben von Formen
- Vector Markup Language (VML), Schlüsselwortfarbnamen
- VML (Vector Markup Language),Schlüsselwortfarbnamen
- Vektorgrafiken, Schlüsselwortfarbnamen
- Schlüsselwortfarbnamen
- Vector Markup Language (VML),RGB-Triplets
- VML (Vector Markup Language),RGB-Triplets
- Vektorgrafiken, RGB-Triplets
- RGB-Triplets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edd8b067f1e3648d2b69f473c02c59392a10b5716afea74b8f7b0c9d093989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057046"
---
# <a name="coloring-shapes"></a>Färben von Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Wie bereits in früheren Abschnitten erwähnt, können Sie "red" verwenden, um eine Farbe in Rot, "blue" für eine Farbe in Blau und so weiter zu darstellen. In diesem Thema wird veranschaulicht, wie Sie Formen in einer beliebigen Farbe zeichnen.

VML erweitert die HTML- und CSS-Farbsyntax. Wenn der Attributtyp eines VML-Elements farblich ist , z. B. **fillcolor** und [](#keyword-color-name) **strokecolor,** können Sie die Farbe ausdrücken, indem Sie entweder einen Schlüsselwortfarbnamen oder ein [RGB-Triplet verwenden.](#rgb-triplet)

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="keyword-color-name"></a>Schlüsselwortfarbname

HTML 4.0 definiert eine Liste von Schlüsselwortfarbnamen. Sie sind "aqua", "black", "blue", "ia", "gray", "green", "lime", "maroon", "violett", "red", "silver", "teal", "white" und "yellow". Der RGB-Wert für diese 16 Farben wird in der [HTML 4.0-Spezifikation definiert.](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5)

Sie können z. B. ein mit Gelb gefülltes Rechteck zeichnen, indem Sie angeben, und ihm eine blaue Kontur geben, indem Sie angeben, wie in der folgenden `fillcolor="yellow"` `strokecolor="blue"` VML-Darstellung gezeigt:

![color1.gif (305 Bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="rgb-triplet"></a>RGB-Triplet

Wenn die Farbe [](#keyword-color-name)kein Schlüsselwortfarbname ist, können Sie die Farbe entweder als RGB-Dezimaldreifach oder als RGB-Hexadezimal-Triplet ausdrücken. Mit RGB-Triplets können Sie Werte für die roten, grünen und blauen Komponenten der Farbe angeben, indem Sie jede Komponente auf einen Wert zwischen 0 und 255 dezimal oder 00 bis FF im Hexadezimalformat festlegen.

Beispielsweise können Sie ein Rechteck erstellen, das mit einer benutzerdefinierten Farbe mit einem RGB-Wert von 253, 249 und 186 als Dezimalzahl gefüllt ist, indem Sie entweder oder angeben, wie in der folgenden `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` VML-Darstellung gezeigt. Im Hexadezimalwert wird der Wert 253 zu FD, 249 zu F9 und 186 zu BA.

![color2.gif (305 Bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Wenn rgb im Hexadezimal-Format ein Muster wie XXYYZZ auftauen kann, können Sie es zu XYZ abkürzen. Beispielsweise kann \# "66FF99" als \# "6F9" geschrieben werden.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

In VML können Sie eine Farbe in einem der folgenden Formate darstellen:

1.  fillcolor="blue"
2.  fillcolor="rgb(0,0,255)"
3.  fillcolor=" \# 0000ff"

 

 