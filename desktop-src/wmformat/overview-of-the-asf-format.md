---
title: Übersicht über das ASF-Format
description: Übersicht über das ASF-Format
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK, Übersicht über das ASF-Format
- Advanced Systems Format (ASF), Format Übersicht
- ASF (Advanced Systems Format), Format Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2858ae1845629c25b52d4c15b5ce7fbb5eb82146
ms.sourcegitcommit: d230e7720c0b566919f8ca11ff7fe3c6b32e028c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "104390070"
---
# <a name="overview-of-the-asf-format"></a>Übersicht über das ASF-Format

Das Advanced Systems Format (ASF) ist ein erweiterbares Dateiformat, das in erster Linie für das Speichern und wiedergeben synchronisierter digitaler Medienströme und die Übertragung über Netzwerke entwickelt wurde. Bei der ASF-Datei handelt es sich um das Containerformat für Windows Media Audio und Windows Media Video basierten Inhalt. Die-Erweiterung WMA oder WMV wird verwendet, um eine ASF-Datei anzugeben, die Inhalte enthält, die mit den Windows Media Audio-und/oder Windows Media Video Codecs codiert sind. Das Windows Media-Format-SDK kann zum Erstellen und Lesen von Windows Media-Dateien sowie von ASF-Dateien verwendet werden, die andere Typen von komprimierten oder unkomprimierten Daten enthalten.

Dieser Abschnitt enthält eine allgemeine Beschreibung des ASF-Formats als Hintergrundinformationen. Da die Reader-und Writer-Objekte alle Low-Level-Dateianalyse-und Formatierungs Aufgaben verarbeiten, ist es nicht erforderlich, ein detailliertes Verständnis von ASF zu haben, bevor Sie dieses SDK zum Erstellen von ASF-Dateien verwenden können. Die gesamte ASF-Spezifikation finden Sie auf der [Microsoft-Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Die Hauptziele des ASF-Formats lauten:

-   Zur Unterstützung der effizienten Wiedergabe von Medienservern, HTTP-Servern und lokalen Speichergeräten.
-   Zur Unterstützung skalierbarer Medientypen wie Audiodaten und Videos.
-   , Um die Präsentation einer einzelnen Multimedia-Komposition über eine breite Bandbreite zu ermöglichen.
-   Ermöglicht das Erstellen von Steuerelementen für Medienstrom Beziehungen, insbesondere in Szenarios mit eingeschränkter Bandbreite.
-   Unabhängig von einem bestimmten Multimedia-Kompositions System, Computerbetriebssystem oder Daten Kommunikationsprotokoll.

Eine ASF-Datei kann mehrere unabhängige oder abhängige Streams enthalten, einschließlich mehrerer Audiodatenströme für Multichannel-Audiodaten oder der Videodaten Ströme mit mehreren Bitraten, die für die Übertragung über verschiedene Bandbreiten geeignet sind. Die Streams können in einem beliebigen komprimierten oder unkomprimierten Format vorliegen. die beste Komprimierung wird jedoch mit den Codecs der Serie Microsoft Windows Media Audio und Video 9 erzielt. Zusätzlich zu den standardstreamtypen für Audiodaten und Video Medien kann eine ASF-Datei auch Textstreams, Webseiten und Skript Befehle sowie beliebige andere beliebige Datentypen enthalten. ASF unterstützt Live-und on-Demand-Multimedia-Inhalte. Sie kann als Vehikel verwendet werden, um h. 32X (z. b. h. 323 und h. 324) oder MBone-Konferenzen aufzuzeichnen oder wiederzugeben.

Eine ASF-Datei ist in Abschnitte organisiert, die als "Objekte" bezeichnet werden. Es gibt drei Objekte der obersten Ebene, ein Header Objekt und ein Datenobjekt (beides erforderlich) sowie ein optionales Index Objekt. Das Header Objekt enthält allgemeine Informationen über die Datei, z. b. die Dateigröße, die Anzahl der Streams, die Fehlerkorrektur Methoden und die verwendeten Codecs. Metadaten werden ebenfalls hier gespeichert. Das Header Objekt ist das einzige Objekt der obersten Ebene, das andere Objekte enthalten kann. Das Datenobjekt enthält die in Paketen organisierten Streamdaten. Das Simple Index-Objekt enthält eine Liste zugeordneter Index/Keyframe-Paare, mit denen Anwendungen eine Datei effizient durchsuchen können. Der Index, der den einzelnen Keyframes zugeordnet ist, kann eine Präsentationszeit, eine Video Frame Nummer oder ein Verweis Zeitstempel sein.

Jedes Objekt der obersten Ebene oder einer niedrigeren Ebene beginnt mit einem Globally Unique Identifier (GUID) und einem Größen Wert. Diese Zahlen ermöglichen es dem Datei Leser, die Informationen an geeigneten Stellen in identifizierbare Objekte zu analysieren. Aufgrund dieser GUIDs können Objekte auf niedrigerer Ebene in beliebiger Reihenfolge gesendet und dennoch erkannt werden. Das ASF-Format ist darauf ausgelegt, einen ungenauen Datenempfang zu überwinden Eine teilweise heruntergeladene ASF-Datei kann noch gelesen werden, solange Sie das Header Objekt und mindestens ein Datenobjekt enthält.

Ausführliche Informationen zu ASF in, dargestellt in der ASF-Spezifikation. Sie können die Spezifikation von der [Microsoft-Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)herunterladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




