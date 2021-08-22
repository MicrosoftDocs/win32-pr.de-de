---
title: Gruppieren von Formen
description: In diesem Artikel wird das Gruppieren von Formen in VML beschrieben, einem Feature, das ab Version Windows Internet Explorer 9 veraltet ist.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Web-Workshop, Gruppieren von Formen
- Entwerfen von Webseiten, Gruppieren von Formen
- Vector Markup Language (VML), Gruppieren von Formen
- VML (Vector Markup Language), Gruppieren von Formen
- Vektorgrafiken, Gruppieren von Formen
- VML-Formen, Gruppierung
- Gruppieren von Formen
- Vector Markup Language (VML),group-Element
- VML (Vector Markup Language),group-Element
- Vektorgrafik,Group-Element
- Gruppenelement
- VML-Elemente, Gruppe
- Vector Markup Language (VML), lokaler Koordinatenraum
- VML (Vector Markup Language),lokaler Koordinatenraum
- Vektorgrafiken, lokaler Koordinatenraum
- lokaler Koordinatenraum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc9ac6da1d38bb6b30f685ebfd0f5a1d9d6026620a0e0c65366ee021668240a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056958"
---
# <a name="grouping-shapes"></a>Gruppieren von Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Wie Sie gelernt haben, können Sie mithilfe von VML ganz einfach einzelne Formen zeichnen. In diesem Abschnitt werden die Vorteile des Gruppierens von Formen und das Gruppieren von Formen erläutert.

Wenn Sie viele Formen hätten, die zusammen skaliert, verschoben oder gedreht werden mussten, wäre es mühsam, die Attribute für jede Form einzeln festlegen zu müssen. Außerdem würden Sie den Rand für Fehler erhöhen. Es wäre besser, wenn Sie die Formen gruppieren und dann die Attribute für die gesamte Gruppe festlegen könnten.

In VML können Sie das -Element verwenden, um viele Formen zu gruppieren, sodass `<group>` sie als eine Einheit transformiert werden können. Beispielsweise können Sie, wie in der folgenden VML-Darstellung gezeigt, problemlos zwei Formen gruppieren.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Wenn Formen gruppiert werden, verwenden sie den [lokalen Koordinatenraum](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) der Gruppe. Daher können Formen innerhalb einer Gruppe skaliert und zusammen verschoben werden. Weitere Beispiele finden Sie im Thema Verwenden des lokalen Koordinatenraums.

Innerhalb einer Gruppe können Sie über so viele Formen oder Gruppen verfügen, wie Sie möchten. Wenn sich eine Gruppe in einer anderen Gruppe befindet, wird sie als "geschachtelte Gruppe" bezeichnet. Es gibt keine Einschränkung für die Schachtelungsebenen.

Die folgenden Zeilen veranschaulichen beispielsweise eine geschachtelte Gruppe mit drei Ebene. Shape3 und Shape4 befinden sich in GroupC. Shape2 und GroupC befinden sich in GroupB. Shape1 und GroupB befinden sich in GroupA.


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



Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858388)

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können das `<group>` -Element verwenden, um viele Formen zu gruppieren, sodass sie als eine Einheit transformiert werden können.

 

 