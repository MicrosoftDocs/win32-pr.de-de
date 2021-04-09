---
title: Häufig gestellte Fragen zu VML
description: Häufig gestellte Fragen zu VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Vector Markup Language (VML), FAQs
- VML (Vector Markup Language), FAQs
- Vektorgrafiken, FAQs
- Vector Markup Language (VML), häufig gestellte Fragen
- VML (Vector Markup Language), häufig gestellte Fragen
- Vektorgrafiken, häufig gestellte Fragen
- Vector Markup Language (VML), GIF-Unterschiede
- VML (Vector Markup Language), GIF-Unterschiede
- Vector Markup Language (VML), PNG-Unterschiede
- VML (Vector Markup Language), PNG-Unterschiede
- Vektorgrafiken, Unterschiede im Raster Format
- Vector Markup Language (VML), XML
- VML (Vector Markup Language), XML
- Vektorgrafiken, XML
- Vector Markup Language (VML), Animation
- VML (Vector Markup Language), Animation
- Vektorgrafiken, Animation
- Vector Markup Language (VML), Macromedia Flash
- VML (Vector Markup Language), Macromedia Flash
- Vektorgrafiken, Macromedia Flash
- Raster Formate
- Animation
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948955"
---
# <a name="frequently-asked-questions-about-vml"></a>Häufig gestellte Fragen zu VML

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

## <a name="does-vml-compete-with-gif-and-png"></a>Konkurriert VML mit GIF und PNG?

Nein. Sowohl GIF als auch PNG sind Raster Formate (oder Bitmapformate), die zum Speichern von Vektorgrafiken verwendet werden können. In den Raster Formaten wird jedes Pixel gespeichert, während Vektorformate wie VML mathematische Beschreibungen oder Gliederungen verwenden, um die Grafiken zu beschreiben. Vektorgrafiken, die in einem vektorbasierten Format gespeichert sind, sind kompakter als die in Raster Formaten gespeicherten Vektorgrafiken, was zu schnelleren Downloadzeiten für Webbenutzer führt.

Außerdem werden VML-Grafiken Inline an die HTML-Seite übermittelt, anstatt sich auf externe Dateien zu verlassen, wie es bei GIF und PNG heute der Fall ist. Dadurch können VML-Grafiken skaliert und mit anderen Webseiten Elementen interagieren, wenn die Größe der Seite geändert wird, sodass die Endbenutzer Leistung verbessert wird.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a>Warum unterstützt Microsoft einen anderen XML-basierten Standard, wenn XML kaum verwendet wird und so jung genug ist?

XML ist eine leistungsstarke, aber einfache Methode, um strukturierte Daten im Web darzustellen und HTML für die Anzeige vollständig zu ergänzen. VML ist ein Beispiel für die vielen anwendungsspezifischen XML-basierten Formate, die in den kommenden Monaten entwickelt und implementiert werden. Beispielsweise wird in der nächsten Version von Office VML verwendet, um HTML-Dokumente mit Anmerkungen zu versehen, um Formatierungsinformationen von Office-Grafik Grafiken zwischen dem systemeigenen Office-Dateiformat und HTML zu erhalten. so können Office-Benutzer nahtlos zwischen den beiden Formaten wechseln.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="who-will-support-vml"></a>Wer wird VML unterstützen?

Wir erwarten, dass viele Lieferanten VML unterstützen. Autodesk, Hewlett-Packard, Macromedia und Visio haben beispielsweise in zukünftigen Versionen ihrer Produkte Unterstützung für VML zugesichert. Microsoft hat Unterstützung für VML in zukünftigen Versionen der Plattformen, wie z. b. Internet Explorer, zugesagt. Außerdem wird VML in der nächsten Generation von Office verwendet, um das "Roundtrip" zwischen dem Office-Format und dem HTML-Code zu aktivieren.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="does-vml-support-animation"></a>Wird die Animation von VML unterstützt?

Nein, dies ist derzeit nicht der Fall. Wir arbeiten jedoch mit unseren VML-Partnern zusammen, um Animations Funktionen im VML-Format hinzuzufügen. Da VML auf XML basiert, kann der Tagsatz problemlos erweitert werden, um zusätzliche Funktionen zu erhalten.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a>Ersetzt VML Macromedia Flash? Hat Macromedia nicht einfach das Flash-Format für Vektorgrafiken an das W3C gesendet?

Nein. VML ist ein textbasiertes Austausch-und Übermittlungs Format für Vektorgrafiken, während Flash ein binäres Format für die Übermittlung von vektorbasierten Grafiken und Animationen ist.

Macromedia hat das Dateiformat nicht an das W3C übermittelt. Allerdings haben Sie das Dateiformat für Anwendungsentwickler, Webentwickler und Endbenutzer geöffnet. Weitere Informationen finden Sie unter <https://www.macromedia.com>.

[Zurück zur VML-Übersicht](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 