---
title: Writer-Objekt
description: Writer-Objekt
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media-Format-SDK, Writer-Objekte
- Advanced Systems Format (ASF), Writer-Objekte
- ASF (Advanced Systems Format), Writer-Objekte
- Objekte, Writer-Objekte
- Writer-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724123"
---
# <a name="writer-object"></a>Writer-Objekt

Das Writer-Objekt wird verwendet, um digitale Mediendateien mit der Dateistruktur Advanced Systems Format (ASF) zu schreiben. Beim Schreiben einer digitalen Mediendatei werden viele interne Schritte für den Writer ausgeführt, mit denen die Komprimierung, die packetisierung und Multiplexing koordiniert werden.

Das Writer-Objekt enthält Schnittstellen für die Ausgabe in Dateien oder ein Netzwerk, unterstützt eine Rückruf Schnittstelle und kann ein oder mehrere Eingabemedien-Eigenschaften Objekte erstellen.

Das Writer-Objekt wird von der [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)-Funktion erstellt, mit der ein Zeiger auf eine **iwmwriter** -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Writer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Writer-Objekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Stellt Methoden zum Generieren von [*DRM*](wmformat-glossary.md) -Schlüsseln bereit.                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | Konfiguriert das Writer-Objekt zum Schreiben einer Datei, die einen vorverschlüsselten Stream enthält, der dem Windows Media DRM 10 for Network Devices-Protokoll entspricht.                                                    |
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Verwaltet die Spezifikation und den Abruf von Header Informationen, z. b. Metadaten, [*Marker*](wmformat-glossary.md)usw.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Verwaltet das Auflisten der verfügbaren Codec-Informationen. Erbt alle Methoden von **iwmheaderinfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Verwaltet das Auflisten der verfügbaren Codec-Informationen. Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.                                                                     |
| [**Iwmwatermarkinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Bietet Zugriff auf Informationen über Wasserzeichen Systeme, die auf dem System vorhanden sind.                                                                                                                          |
| [**Iwmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Startet und beendet das Schreiben von ASF-Dateien. Es enthält Methoden zum Zuordnen von Puffern, festlegen und Abrufen von Eingabe Eigenschaften, Festlegen von Profilen und Ausgabe Dateinamen und Entsperren des Writers.         |
| [**Iwmschreibadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Fügt angegebene Sink-Objekte hinzu, ruft Sie ab und entfernt Sie. Ruft Statistiken, die Anzahl der senken und die Uhrzeit ab, zu der der Writer arbeitet. und führt andere erweiterte Funktionen aus.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Bietet einige erweiterte Funktionen, insbesondere für die Handhabung von Deinterlacing-Videos. Erbt alle Methoden von **iwmschreiteradvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Bietet zusätzliche Writer-Funktionen, einschließlich der Möglichkeit, ausführliche Writer-Statistiken zu erhalten. Erbt alle Methoden von **iwmschreiteradvanced** und **IWMWriterAdvanced2**.                       |
| [**Iwmbeschreiterpostview**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Verwaltet einige erweiterte Schreibfunktionen im Zusammenhang mit Postview-Beispielen. Bei der nach Anzeige wird die Ausgabe, normalerweise von einem Encoder, angezeigt, um zu überprüfen, ob der Codierungs-/Decodierungs Prozess ordnungsgemäß |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Verwaltet Vorverarbeitungs Durchläufen, die vom Writer erstellt werden. Vorverarbeitungs Durchläufen werden verwendet, um die Qualität der codierten Ausgabe zu verbessern.                                                                                  |



 

Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, um den Fortschritt der Post Ansicht zu verfolgen.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Iwmschreiterpostviewcallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Verwaltet, wie unkomprimierte Beispiele vom Writer-Objekt empfangen werden, um die Vorschau der Vorgänge des Codecs anzuzeigen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




