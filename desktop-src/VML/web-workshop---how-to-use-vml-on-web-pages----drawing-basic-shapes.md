---
title: Zeichnen von grundlegenden Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Webworkshop, Zeichnen von Formen
- Entwerfen von Webseiten, Zeichnen von Formen
- Vector Markup Language (VML), Zeichnen von Formen
- VML (Vector Markup Language), Zeichnen von Formen
- Vektorgrafiken, Zeichnungsformen
- Zeichnen von Formen
- VML-Formen, zeichnen
- Vector Markup Language (VML), XML
- VML (Vector Markup Language), XML
- Vektorgrafiken, XML
- Vector Markup Language (VML), CSS2
- VML (Vector Markup Language), CSS2
- Vektorgrafiken, CSS2
- Vector Markup Language (VML), Elemente
- VML (Vector Markup Language), Elemente
- Vektorgrafiken, Elemente
- VML-Elemente, Zeichnen von Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474012"
---
# <a name="drawing-basic-shapes"></a>Zeichnen von grundlegenden Formen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie einfach es ist, eine Form mithilfe von VML zu zeichnen.

Zum Erstellen eines roten Oval auf einer Webseite, wie in der folgenden Abbildung gezeigt, können Sie das Oval mit einem Grafik Bearbeitungs Tool zeichnen, die Zeichnung als Bitmap speichern und dann die Bitmap auf der Webseite einfügen:

![oval1.gif (627 Bytes)](images/oval1.gif)

Alternativ können Sie mit VML Grafiken zeichnen. Im vorherigen Beispiel können Sie die folgenden Zeilen in der `<BODY>` Region der Webseite eingeben, um das rote Oval zu zeichnen:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` und `</v:...>` sind das Starttag und das Endtag in der [XML-Syntax](#xml-structure).`style='width:100pt; height:75pt'` stellt [CSS-Informationen](#css-information)bereit. **Oval** und **FillColor**= "Red" sind [VML-Elemente](#vml-elements).

Sie können die Grafiken ändern, indem Sie einfach Ihre Eigenschafts Attribute in VML ändern. Wenn Sie im vorherigen Beispiel zu wechseln, `fillcolor="red"` `fillcolor="blue"` wie in der folgenden VML-Darstellung gezeigt, ändert sich das rote Oval in blau:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Browser, die VML unterstützen, können die in VML dargestellten Grafiken renderten und anzeigen, ohne separate Bilddateien herunterladen zu müssen. Die meisten in VML dargestellten Grafiken werden in Browsern schneller gerendert und erfordern weniger Speicherplatz und Downloadzeit.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="xml-structure"></a>XML-Struktur

VML wird gemäß den Regeln der Extensible Markup Language (XML) formatiert. Jeder Standard-XML-Parser kann VML analysieren und die resultierenden Daten an einen VML-spezifischen Prozessor übergeben. Wenn Sie den Browsern mitteilen möchten, wie Daten an einen VML-spezifischen Prozessor übergeben werden, müssen Sie einige Informationen eingeben, wie z. b. [Namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) und [eingebettete benutzerdefinierte Objekte](web-workshop---how-to-use-vml-on-web-pages----appendix.md). Anschließend können Sie mit VML Grafiken in der `<BODY>` Region wie im vorherigen Beispiel eingeben.

`"v:"`Mit dem Präfix für jedes XML-Tag wird das Tag als VML identifiziert. Das `"v:"` Präfix in der `<BODY>` Region sollte mit übereinstimmen `<html xmlns:v="...">` .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="css-information"></a>CSS-Informationen

VML verwendet [Cascading Stylesheets, Ebene 2 (CSS2),](https://www.w3.org/TR/PR-CSS2/) um die Größe der Grafiken zu bestimmen und die Grafiken auf einer Webseite zu positionieren. Im vorherigen Beispiel haben wir die Größe des Oval als 100 Punkte (Breite) um 75 Punkte (Höhe) ( `style='width:100pt;height:75pt'` ) angegeben.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="vml-elements"></a>VML-Elemente

Im vorherigen Beispiel haben wir ein vordefiniertes VML-Element verwendet, `<oval>` um ein Oval zu zeichnen. Anschließend haben wir das **FillColor** -Eigenschafts Attribut des- `<oval>` Elements verwendet, um das Oval in rot auszufüllen.

Basierend auf dem [Starttags-, Endtags-und Empty-Element Tags-](https://www.w3.org/TR/REC-xml#sec-starttags) Abschnitt der [Spezifikation von XML 1,0](https://www.w3.org/TR/REC-xml)können leere Element Tags für alle Elemente verwendet werden, die über keinen Inhalt verfügen. Beispielsweise gibt es in der folgenden VML-Darstellung keinen Inhalt (Unterelement) innerhalb des- `<oval>` Elements. (Beachten Sie, dass **Stil** und **FillColor** die Attribute des- `<oval>` Elements sind; Sie sind keine unter Elemente.)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Daher können Sie das Tag "Empty-Element" verwenden, wie in der folgenden VML-Darstellung dargestellt, um das gleiche Element wie die obige Zeile darzustellen.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können VML verwenden, um Grafiken auf einer Webseite zu zeichnen, und dann diese Grafiken anpassen, indem Sie einfach Ihre Eigenschafts Attribute ändern. Außerdem werden die meisten in VML dargestellten Grafiken schneller in Browsern gerendert und benötigen weniger Downloadzeit und Speicherplatz.

 

 