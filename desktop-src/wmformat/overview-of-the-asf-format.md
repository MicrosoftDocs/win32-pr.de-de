---
title: Übersicht über das ASF-Format
description: Übersicht über das ASF-Format
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK, Übersicht über das ASF-Format
- Advanced Systems Format (ASF), Formatübersicht
- ASF (Advanced Systems Format), Formatübersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee075330e9c68ef1fbdadea12c70fd8deec584f99f8dadd31cb55070dc11eee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930560"
---
# <a name="overview-of-the-asf-format"></a>Übersicht über das ASF-Format

Das Advanced Systems Format (ASF) ist ein erweiterbares Dateiformat, das hauptsächlich zum Speichern und Wiedergeben synchronisierter digitaler Medienstreams und deren Übertragung über Netzwerke entwickelt wurde. ASF ist das Containerformat für Windows Medienaudio und Windows Medienvideoinhalte. Die Erweiterung wma oder wmv wird verwendet, um eine ASF-Datei anzugeben, die Inhalte enthält, die mit den Windows Medienaudio- und/oder Windows Media Video-Codecs codiert sind. Das Windows Media Format SDK kann verwendet werden, um Windows Mediendateien sowie ASF-Dateien zu erstellen und zu lesen, die andere Typen komprimierter oder nicht komprimierter Daten enthalten.

Dieser Abschnitt enthält eine allgemeine Beschreibung des ASF-Formats als Hintergrundinformationen. Da die Reader- und Writer-Objekte alle Dateiparsing- und Formatierungsaufgaben auf niedriger Ebene verarbeiten, ist es nicht erforderlich, vor der Verwendung dieses SDK zum Erstellen von ASF-Dateien ein detailliertes Verständnis von ASF zu haben. Die vollständige ASF-Spezifikation finden Sie auf der [Microsoft-Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Die Hauptziele des ASF-Formats sind:

-   Zur Unterstützung der effizienten Wiedergabe von Medienservern, HTTP-Servern und lokalen Speichergeräten.
-   Zur Unterstützung skalierbarer Medientypen wie Audio und Video.
-   Damit eine einzelne Multimediakomposition über eine Vielzahl von Bandbreiten dargestellt werden kann.
-   Um die Erstellung der Kontrolle über Mediendatenstrombeziehungen zu ermöglichen, insbesondere in Szenarien mit eingeschränkter Bandbreite.
-   Um unabhängig von einem bestimmten Multimediakompositionssystem, Computerbetriebssystem oder Datenkommunikationsprotokoll zu sein.

Eine ASF-Datei kann mehrere unabhängige oder abhängige Datenströme enthalten, einschließlich mehrerer Audiostreams für Mehrkanalaudiodaten oder Videostreams mit mehreren Bitraten, die für die Übertragung über verschiedene Bandbreiten geeignet sind. Die Streams können in einem beliebigen komprimierten oder unkomprimierten Format vorliegen. Die beste Komprimierung wird jedoch mit den Codecs der Microsoft Windows Media Audio- und Video 9-Serie erzielt. Zusätzlich zu den Standarddatenstromtypen für Audio- und Videomedien kann eine ASF-Datei auch Textstreams, Webseiten und Skriptbefehle sowie beliebige andere Datentypen enthalten. ASF unterstützt Live- und on-Demand-Multimediainhalte. Sie kann als Fahrzeug zum Aufzeichnen oder Wiedergeben von H.32X-Konferenzen (z.B. H.323 und H.324) oder MBONE-Konferenzen verwendet werden.

Eine ASF-Datei ist in Abschnitte unterteilt, die als "Objekte" bezeichnet werden. Es gibt drei Objekte der obersten Ebene, ein Header-Objekt und ein Data-Objekt (beide erforderlich) sowie ein optionales Index-Objekt. Das Header-Objekt enthält allgemeine Informationen zur Datei, z. B. Dateigröße, Anzahl von Streams, Fehlerkorrekturmethoden und verwendete Codecs. Metadaten werden hier ebenfalls gespeichert. Das Header-Objekt ist das einzige Objekt der obersten Ebene, das andere Objekte enthalten kann. Das Data-Objekt enthält die in Paketen organisierten Streamdaten. Das Simple Index-Objekt enthält eine Liste der zugeordneten Index-/Keyframe-Paare, mit denen Anwendungen eine Datei effizient durchsuchen können. Der jedem Keyframe zugeordnete Index kann eine Präsentationszeit, eine Videoframenummer oder ein Verweiszeitstempel sein.

Jedes Objekt der obersten ebene oder niedrigeren Ebene beginnt mit einem global eindeutigen Bezeichner (GLOBALLY UNIQUE Identifier, GUID) und einem Größenwert. Diese Zahlen ermöglichen es dem Dateileser, die Informationen an geeigneten Stellen in identifizierbare Objekte zu analysieren. Aufgrund dieser GUIDs können Objekte auf niedrigerer Ebene in beliebiger Reihenfolge gesendet und weiterhin erkannt werden. Das ASF-Format wurde entwickelt, um ungenauen Datenempfang zu umgehen. Eine teilweise heruntergeladene ASF-Datei kann weiterhin gelesen werden, solange sie das Header-Objekt und mindestens ein Data-Objekt enthält.

Ausführliche Informationen zu ASF in in der ASF-Spezifikation. Sie können die Spezifikation von der [Microsoft-Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)herunterladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




