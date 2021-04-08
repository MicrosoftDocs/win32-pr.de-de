---
title: Verwenden des lokalen Koordinaten Raums
description: Verwenden des lokalen Koordinaten Raums
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Webworkshop, lokaler Koordinaten Bereich
- Entwerfen von Webseiten, lokaler Koordinaten Bereich
- Vector Markup Language (VML), lokaler Koordinaten Bereich
- VML (Vector Markup Language), lokaler Koordinaten Bereich
- Vektorgrafiken, lokaler Koordinatenraum
- lokaler Koordinaten Bereich
- VML-Formen, lokaler Koordinaten Bereich
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language), Gruppieren von Formen
- Vektorgrafiken, Gruppierungs Formen
- VML-Formen, gruppieren
- Gruppieren von Formen
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
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729736"
---
# <a name="using-local-coordinate-space"></a>Verwenden des lokalen Koordinaten Raums

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wie Sie gelernt haben, können Sie die Attribute " **Width** " und " **height** " angeben, um die Größe eines enthaltenden Felds zu definieren, in dem der Inhalt einer Form oder Gruppe gerendert wird. In diesem Thema wird erläutert, was der lokale Koordinaten Bereich ist und wie er in VML zum Skalieren von Formen verwendet wird.

Wenn Sie aufgefordert werden, ein 1-Zoll-Rechteck mit zwei Zoll in einem Raster Papier zu zeichnen, müssen Sie zunächst herausfinden, wo Sie beginnen sollen (der Ausgangspunkt). Anschließend würden Sie herausfinden, wie Sie den Zellen des Raster Papiers (der Koordinate) einen Zoll zuordnen.

Ebenso müssen, wenn der Inhalt einer Form oder Gruppe in das enthaltende Feld auf einer Webseite gerendert wird, der Ursprungs Punkt und die Koordinate definiert werden. VML bietet lokalen Koordinaten Bereich, damit jede Form oder Gruppe ihren eigenen Ausgangspunkt und ihre eigenen Koordinaten definieren kann. Wenn Sie keinen Koordinaten Bereich angeben, wird der Standardwert verwendet. Standardmäßig beginnt der Ursprung in der linken oberen Ecke des enthaltenden Felds.

Die VML-Darstellung für das unten gezeigte rote Oval gibt z. b. nicht die **coordsize** -Eigenschaft und die **coordorigin** -Eigenschafts Attribute an. Daher wird ein lokaler Standard Koordinaten Bereich verwendet. Die Größe des Oval beträgt 100 Punkte (Breite) um 75 Punkte (Höhe). Sie können die Größe des Oval ändern, indem Sie eine andere Breite oder Höhe angeben, wie Sie im Thema [Skalierungs Formen](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) gelernt haben.

![oval1.gif (627 Bytes)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Wenn die Form komplizierter wird, oder wenn Sie mehrere Formen gruppieren und diese zentral hochskalieren möchten, sollten Sie die in VML bereitgestellte lokale Koordinatenraum Funktion verwenden.

Für jede Form oder Gruppe können Sie die Eigenschafts Attribute **coordsize** und **coordorigin** verwenden, um den lokalen Koordinaten Bereich der Form oder Gruppe zu definieren. Das **coordsize** -Attribut gibt die Anzahl der Einheiten entlang der Breite und die Höhe des enthaltenden Felds an. Das **coordorigin** -Attribut definiert die Koordinate in der oberen linken Ecke des enthaltenden Felds. Alle Positions bezogenen Informationen (z. b. "width", "Height", "Left", "Top", "Path" usw.) werden im Hinblick auf die Einheit im lokalen Koordinatenraum ausgedrückt.

So definiert z. b. wie in der folgenden VML-Darstellung gezeigt `width: 100pt; height: 100pt;` die Größe des enthaltenden Felds, sodass die Form 100 Punkte um 100 Punkte ist.

![cord1.gif (836 bytes)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` definiert die Größe des lokalen Koordinaten Raums für die Form von 21600 Einheiten um 21600 Einheiten. Aus diesem Grund ist eine Einheit im lokalen Koordinaten Bereich gleich dem 1/216-Punkt.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` definiert den Umriss der Form als Rautenform. Wir haben gelernt, dass alle Positions bezogenen Informationen (z. b. "width", "Height", "Left", "Top", "Path" usw.) im Hinblick auf die Einheit im lokalen Koordinatenraum ausgedrückt werden. Daher bedeutet 10800 in der `<path>` 10800-Einheiten, was 50 Punkten entspricht.

Wenn Sie die Größe dieser Rautenform ändern möchten, geben Sie einfach eine andere Breite oder Höhe an. Sie müssen keinen Wert in der ändern `<path>` . Wenn Sie die Funktion für den lokalen Koordinatenraum nicht verwendet haben, müssen Sie für diese komplizierte Form jeden Wert in der ändern, wenn Sie die Größe ändern möchten `<path>` .

Beispielsweise können Sie die Rautenform skalieren, indem Sie einfach eine andere Breite oder Höhe angeben, wie in der folgenden VML-Darstellung dargestellt:

![cord2.gif (1692 Bytes)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





Sie können auch den lokalen Koordinaten Bereich im- `<group>` Element verwenden, damit der Inhalt aller Formen innerhalb der Gruppe entsprechend der gleichen Koordinate zentral hochskaliert wird. Wenn Sie dann eine Gruppe von Formen skalieren oder verschieben möchten, ändern Sie einfach die Einstellungen für Breite und Höhe bzw. **coordsize** und **coordorigin** der Gruppe.

In der folgenden VML-Darstellung wird z `<v:group style='... width:200pt;height:200pt;'>` . b. die Größe des enthaltenden Felds für die Gruppe mit 200 Punkten um 200 Punkte definiert.

![cord3.gif (645 bytes)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` definiert die Größe des lokalen Koordinaten Raums für die Gruppe, um 1000 Einheiten um 1000 Einheiten zu sein. Daher entspricht eine Einheit im lokalen Koordinaten Bereich dem 1/5-Punkt.
-   `coordorigin="-500,-500"` definiert die linke obere Ecke des enthaltenden Felds als "-500,-500". Daher reicht das Koordinatensystem in der enthaltenden Box zwischen-500 und 500 entlang der x-Achse und-500 bis 500 entlang der y-Achse. Anders ausgedrückt: die Mitte des enthaltenden Felds ist "0,0".
-   `<v:oval style='... width:400;height:300;'>` definiert die Größe des enthaltenden Felds für das rote Oval um 400 Einheiten (Breite) um 300 Einheiten (Höhe). Da eine Einheit im lokalen Koordinaten Bereich 1/5 Punkt entspricht, ist die Größe des enthaltenden Felds für das rote Oval 80 Punkte (Breite) um 60 Punkte (Höhe).

Ebenso ist die Größe des enthaltenden Felds für das grüne roundRect 50 Punkte (Breite) um 40 Punkte (Höhe).

Wenn Sie die Größe des roten oval und des grünen roundrects ändern möchten, ändern Sie einfach `<v:group style='... width:200pt;height:200pt;'>` . Das ist das, und Sie müssen die Größe der beiden Formen nicht einzeln ändern.

Wenn Sie z. b. `<v:group style='... width:200pt;height:200pt;'>` in ändern `<v:group style='... width:300pt;height:300pt;'>` , werden die Formen größer, wie in der folgenden Abbildung dargestellt:

![cord4.gif (943 bytes)](images/cord4.gif)



Sie werden auch bemerken, dass sich die Formen anders befinden. Dies liegt daran, dass die Formen von "0,0" gezeichnet werden, das sich in der Mitte des enthaltenden Felds befindet. Da Sie das enthaltende Feld vergrößern, wird der Mittelpunkt des enthaltenden Felds ebenfalls verschoben.

Wenn Sie `coordorigin="-500,-500"` zu wechseln `coordorigin="0,0"` , wie in der folgenden Abbildung gezeigt, werden Sie feststellen, dass das rote oval und das grüne roundRect jeweils an die neue Position verschoben werden. Der Grund hierfür ist, dass "0, 0" nun in der oberen linken Ecke des enthaltenden Felds angezeigt wird.

![cord5.gif (648 Bytes)](images/cord5.gif)



Es ist auch wichtig zu beachten, dass das enthaltende Feld keinen Clippingbereich festlegt. Grafiken können außerhalb der Grenzen des enthaltenden Felds gezeichnet werden. Das enthaltende Feld dient lediglich zum Zuordnen des lokalen Koordinaten Raums zum Seiten Raum.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 