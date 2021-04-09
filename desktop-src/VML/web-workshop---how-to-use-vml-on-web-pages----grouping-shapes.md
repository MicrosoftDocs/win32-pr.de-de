---
title: Gruppieren von Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Webworkshop, Gruppieren von Formen
- Entwerfen von Webseiten, Gruppieren von Formen
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language), Gruppieren von Formen
- Vektorgrafiken, Gruppierungs Formen
- VML-Formen, gruppieren
- Gruppieren von Formen
- Vector Markup Language (VML), Group-Element
- VML (Vector Markup Language), Group-Element
- Vektorgrafiken, Group-Element
- Gruppenelement
- VML-Elemente,-Gruppe
- Vector Markup Language (VML), lokaler Koordinaten Bereich
- VML (Vector Markup Language), lokaler Koordinaten Bereich
- Vektorgrafiken, lokaler Koordinatenraum
- lokaler Koordinaten Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039508"
---
# <a name="grouping-shapes"></a>Gruppieren von Formen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wie Sie gelernt haben, können Sie einfach einzelne Formen mithilfe von VML zeichnen. In diesem Abschnitt werden die Vorteile der Gruppierung von Formen und das Gruppieren von Formen erläutert.

Wenn Sie über viele Formen verfügen, die skaliert, verschoben oder gedreht werden mussten, wäre es mühsam, die Attribute für jede Form einzeln festzulegen. Außerdem würden Sie den Rand für Fehler erhöhen. Es wäre besser, wenn Sie die Formen gruppieren und dann die Attribute für die gesamte Gruppe festlegen.

In VML können Sie das- `<group>` Element verwenden, um viele Formen zu gruppieren, sodass Sie als eine Einheit transformiert werden können. Beispielsweise können Sie, wie in der folgenden VML-Darstellung gezeigt, zwei Formen problemlos gruppieren.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Wenn Formen gruppiert sind, verwenden Sie den [lokalen Koordinaten Bereich](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) der Gruppe. Daher können Formen innerhalb einer Gruppe skaliert und gruppiert werden. Weitere Beispiele finden Sie im Thema Verwenden von lokalem Koordinatenraum.

Innerhalb einer Gruppe können Sie beliebig viele Formen oder Gruppen haben. Wenn sich eine Gruppe in einer anderen Gruppe befindet, wird Sie als "geschachtelte Gruppe" bezeichnet. Es gibt keine Einschränkung für die Schachtelungs Ebenen.

In den folgenden Zeilen wird z. b. eine Gruppierungs Gruppe mit drei Ebenen veranschaulicht. Shape3 und Shape4 befinden sich in groupc. Shape2 und groupc sind in GroupB. Shape1 und GroupB sind in groupA.


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können das- `<group>` Element verwenden, um viele Formen zu gruppieren, sodass Sie als eine Einheit transformiert werden können.

 

 