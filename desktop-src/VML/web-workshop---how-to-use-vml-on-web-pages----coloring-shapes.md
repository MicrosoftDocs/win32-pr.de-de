---
title: Farbformen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Webworkshop, Farbformen
- Entwerfen von Webseiten, Farbformen
- Vector Markup Language (VML), Farbformen
- VML (Vector Markup Language), Farbformen
- Vektorgrafiken, Farbformen
- VML-Formen, Farben
- Farbformen
- Vector Markup Language (VML), Schlüsselwort Farben Namen
- VML (Vector Markup Language), Name der Schlüsselwort Farbe
- Vektorgrafiken, Schlüsselwort Farben Namen
- Farbnamen für Schlüsselwort
- Vector Markup Language (VML), RGB-dreier
- VML (Vector Markup Language), RGB-drei
- Vektorgrafiken, RGB-dreier
- RGB-dreier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039293"
---
# <a name="coloring-shapes"></a>Farbformen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wie in den vorherigen Abschnitten erwähnt, können Sie "Red" verwenden, um eine Farbe in rot darzustellen, "blau", um eine Farbe in blau darzustellen usw. In diesem Thema wird veranschaulicht, wie Formen in einer beliebigen Farbe gezeichnet werden.

VML erweitert die HTML-und CSS-Farb Syntax. Wenn der Attributtyp eines VML-Elements Farben ist (z. b. **FillColor** und **strokeColor** ), können Sie die Farbe entweder mithilfe eines [Schlüssel Worts-Farbnamens](#keyword-color-name) oder eines [RGB-Dreiecks](#rgb-triplet)Ausdrücken.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="keyword-color-name"></a>Name der Schlüsselwort Farbe

HTML 4,0 definiert eine Liste von Schlüsselwort Farben. Dabei handelt es sich um Aqua, Black, Blue, Fuchsia, Gray, Green, Kalk, Maroon, Navy, Olive, lila, rot, Silber, Teal, weiß und gelb. Der RGB-Wert für diese 16 Farben wird in der [Spezifikation von HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) definiert.

Sie können z. b. ein Rechteck mit gelb zeichnen, indem Sie angeben `fillcolor="yellow"` , und einen blauen Umriss angeben, indem Sie angeben `strokecolor="blue"` , wie in der folgenden VML-Darstellung gezeigt:

![color1.gif (305 Bytes)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="rgb-triplet"></a>RGB-dreier

Wenn es sich bei der Farbe nicht um einen [Schlüsselwort Farbnamen](#keyword-color-name)handelt, können Sie die Farbe entweder als RGB-Dezimalzahl oder als RGB-hexadezimal Trennzeichen Ausdrücken. Mit RGB-Werten können Sie Werte für die roten, grünen und blauen Komponenten der Farbe angeben, wobei jede Komponente auf einen Wert zwischen 0 und 255 in Dezimalwert oder 00 bis FF im Hexadezimal Bereich festgelegt wird.

Sie können z. b. ein Rechteck erstellen, das mit einer angepassten Farbe mit einem RGB-Wert von 253, 249, 186 in Dezimalform aufgefüllt ist, indem Sie entweder `fillcolor="rgb(253,249, 186)"` oder angeben `fillcolor="#FDF9BA"` , wie in der folgenden VML-Darstellung gezeigt. In Hexadezimal wird der Wert 253 zu FD, 249 wird zu F9, und 186 wird zu BA.

![color2.gif (305 Bytes)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Wenn der RGB-Wert im Hexadezimal Format über ein Muster wie xxyyzz verfügt, können Sie es mit XYZ abkürzen. Beispielsweise kann " \# 66ff99" als " \# 6f9" ausgeschrieben werden.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

In VML können Sie eine Farbe in einem der folgenden Formate darstellen:

1.  FillColor = "Blue"
2.  FillColor = "RGB (0, RGB)"
3.  FillColor = " \# 0000FF"

 

 