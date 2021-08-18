---
title: Zeichnen grundlegender Formen
description: In diesem Artikel wird das Zeichnen grundlegender Formen in VML beschrieben, einem Feature, das ab Version 9 Windows Internet Explorer ist.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web-Workshop,Zeichnen von Formen
- Entwerfen von Webseiten, Zeichnen von Formen
- Vector Markup Language (VML), Zeichnen von Formen
- VML (Vector Markup Language), Zeichnen von Formen
- Vektorgrafiken,Zeichnen von Formen
- Zeichnen von Formen
- VML-Formen, Zeichnen
- Vector Markup Language (VML),XML
- VML (Vector Markup Language),XML
- Vektorgrafik, XML
- Vector Markup Language (VML),CSS2
- VML (Vector Markup Language),CSS2
- Vektorgrafiken,CSS2
- Vector Markup Language (VML),Elemente
- VML (Vector Markup Language),Elemente
- Vektorgrafiken,Elemente
- VML-Elemente, Zeichnen von Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4a8b7985371d9cffc6e7359cef1a17c69c403c7802de458b68d9df8c36e3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136923"
---
# <a name="drawing-basic-shapes"></a>Zeichnen grundlegender Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie einfach es ist, eine Form mithilfe von VML zu zeichnen.

Um ein rotes Oval auf einer Webseite zu erstellen, wie in der folgenden Abbildung dargestellt, können Sie das Oval mithilfe eines Grafischen Bearbeitungstools zeichnen, Ihre Zeichnung als Bitmap speichern und die Bitmap dann auf Ihrer Webseite einfügen:

![oval1.gif (627 Bytes)](images/oval1.gif)

Alternativ können Sie VML verwenden, um Grafiken zu zeichnen. Im vorherigen Beispiel können Sie die folgenden Zeilen in den Bereich ihrer Webseite eingeben, um das rote Oval `<BODY>` zu zeichnen:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>`und `</v:...>` sind das Start- und Endtag in der [XML-Syntax.](#xml-structure)`style='width:100pt; height:75pt'` stellt [CSS-Informationen zur Verfügung.](#css-information) **oval** und **fillcolor**="red" sind [VML-Elemente.](#vml-elements)

Sie können die Grafiken ändern, indem Sie einfach deren Eigenschaftsattribute in VML ändern. Wenn Sie im vorherigen Beispiel in ändern, wie in der folgenden VML-Darstellung gezeigt, ändert sich das rote `fillcolor="red"` `fillcolor="blue"` Oval in Blau:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Browser, die VML unterstützen, können die in VML dargestellten Grafiken rendern und anzeigen, ohne separate Bilddateien herunterladen zu müssen. Die meisten in VML dargestellten Grafiken werden in Browsern schneller gerendert und erfordern weniger Speicherplatz und Downloadzeit.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="xml-structure"></a>XML-Struktur

VML wird gemäß den Regeln von Extensible Markup Language (XML) formatiert. Jeder XML-Standardparser kann VML analysieren und die resultierenden Daten an einen VML-spezifischen Prozessor aushingen. Damit die Browser wissen, wie Daten an einen VML-spezifischen Prozessor übergefertigt werden, müssen Sie einige Informationen wie [Namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) und eingebettete benutzerdefinierte [Objekte eingeben.](web-workshop---how-to-use-vml-on-web-pages----appendix.md) Anschließend können Sie VML verwenden, um Grafiken wie im vorherigen Beispiel in der `<BODY>` Region ein typ zu geben.

Das `"v:"` Präfix für jedes XML-Tag identifiziert das Tag als VML. Das `"v:"` Präfix in der Region sollte mit konsistent `<BODY>` `<html xmlns:v="...">` sein.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="css-information"></a>CSS-Informationen

VML verwendet [Cascading Stylesheets, Ebene 2 (CSS2),](https://www.w3.org/TR/PR-CSS2/) um die Größe der Grafiken zu bestimmen und die Grafiken auf einer Webseite zu positionieren. Im vorherigen Beispiel haben wir die Größe des Ovals als 100 Punkte (Breite) um 75 Punkte (Höhe) ( ) `style='width:100pt;height:75pt'` angegeben.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="vml-elements"></a>VML-Elemente

Im vorherigen Beispiel haben wir ein vordefiniertes VML-Element `<oval>` verwendet, um ein Oval zu zeichnen. Anschließend haben wir das **fillcolor-Eigenschaftsattribut** des Elements verwendet, um das Oval mit Rot zu `<oval>` füllen.

Basierend auf [dem Abschnitt Start-Tags, Endtags](https://www.w3.org/TR/REC-xml#sec-starttags) und Empty-Element Tags der [XML 1.0-Spezifikation](https://www.w3.org/TR/REC-xml)können leere Elementtags für jedes Element ohne Inhalt verwendet werden. Wie in der folgenden VML-Darstellung gezeigt, gibt es beispielsweise keinen Inhalt (Unterelement) innerhalb des `<oval>` -Elements. (Beachten Sie, **dass stil** und **fillcolor** die Attribute des Elements `<oval>` sind. Sie sind keine Unterelemente.)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Daher können Sie das Empty-Element-Tag wie in der folgenden VML-Darstellung gezeigt verwenden, um dasselbe wie in der obigen Zeile zu repräsentieren.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können VML verwenden, um Grafiken auf einer Webseite zu zeichnen, und diese Grafiken dann anpassen, indem Sie einfach deren Eigenschaftenattribute ändern. Außerdem werden die meisten in VML dargestellten Grafiken in Browsern schneller gerendert, und der Download nimmt weniger Zeit und Speicherplatz auf dem Datenträger ein.

 

 