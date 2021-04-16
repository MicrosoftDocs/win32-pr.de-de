---
title: SDK für Windows Media-Format 11
description: SDK für Windows Media-Format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media-Format-SDK, Informationen zu
- Windows Media SDK
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Informationen zu
- ASF (Advanced Systems Format), Informationen zu
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, wichtige Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474548"
---
# <a name="windows-media-format-11-sdk"></a>SDK für Windows Media-Format 11

Diese Dokumentation beschreibt das Microsoft Windows Media-Format Software Development Kit (SDK) und gilt für die 32-Bit-und x64-basierten Versionen des SDK.

Das Windows Media-Format-SDK ist eine Komponente des Microsoft Windows Media Software Development Kit (SDK). Weitere Komponenten sind das Windows Media Services SDK, das Windows Media Encoder SDK, das Windows Media Rights Manager SDK, das Windows Media Device Manager SDK und das Windows Media Player SDK.

Das Windows Media-Format SDK bietet Anwendungsentwicklern Zugriff auf die Komponenten des Windows Media-Formats. Diese Komponenten umfassen den Datei Container "Advanced Systems Format (ASF)", die Windows Media Audio und Video Codecs, grundlegende netzwerkstreamingfunktion und Digital Rights Management. Die Objekte des Windows Media Format SDK bearbeiten die Komponenten von Windows-Medien auf niedriger Ebene. die anderen Komponenten des Windows Media SDK enthalten Objekte, die auf einer höheren Ebene funktionieren.

Der Hauptzweck des Windows Media-Format-SDKs besteht darin, Entwicklern das Erstellen von Anwendungen zu ermöglichen, die die Dateien und Netzwerkstreams von Advanced Systems Format (ASF) abspielen, schreiben, bearbeiten, verschlüsseln und bereitzustellen. Diese Dateien und Streams enthalten häufig Audioinhalte und Videoinhalte, die mit den Windows Media Audio-und Video Codecs codiert werden. Allerdings kann ASF beliebige Datentypen enthalten. Weitere Informationen zur Containerstruktur "Advanced Systems Format" finden Sie unter [Übersicht über das ASF-Format](overview-of-the-asf-format.md).

Die wichtigsten Features des Windows Media SDK sind:

-   Unterstützung für branchenführende Codecs. Das Windows Media Format 11 SDK enthält den Microsoft Windows Media Video 9-Codec und den Microsoft Windows Media Audio 9,1-Codec. Beide Codecs stellen eine außergewöhnliche Codierung digitaler Medieninhalte bereit. Neu in dieser Version ist der Windows Media Video 9 Advanced Profile Codec, der Optimierungen für Broadcast Videos bereitstellt. Dieses SDK enthält auch den Microsoft Windows Media Video 9-Bildschirm Codec zum Komprimieren von Computerbildschirm Aktivitäten während der Sitzungen von Benutzer Anwendungen und den Windows Media Audio 9,1-Sprach Codec, der Low-Komplexitäts-AudioCodes, wie z. b. Sprache, codiert und sich intelligent an komplexere Audiodaten wie Musik anpasst, um eine bessere Darstellung von kombinierten Sprach Musik Szenarien zu erhalten.
-   Unterstützung für das Schreiben von ASF-Dateien. Dateien werden basierend auf anpassbaren Profilen erstellt und ermöglichen eine einfache Konfiguration und Standardisierung von Dateien. Dieses SDK kann zum Schreiben von Dateien verwendet werden, die mehr als 2 Gigabyte umfassen, sodass Sie längere, qualitativ hochwertige und kontinuierliche Dateien ermöglichen.
-   Unterstützung für das Lesen von ASF-Dateien. Dieses SDK bietet Unterstützung für das Lesen von lokalen ASF-Dateien sowie das Lesen von ASF-Daten, die über ein Netzwerk gestreamt werden. Unterstützung wird auch für viele erweiterte Lesefunktionen bereitgestellt, wie z. b. systemeigene Unterstützung für MBR-Dateien (Multiple Bitrate), die mehrere Datenströme mit demselben Inhalt enthalten, die mit unterschiedlichen Bitraten codiert sind Der Reader wählt automatisch den zu verwendenden MBR-Stream aus, abhängig von der verfügbaren Bandbreite zum Zeitpunkt der Wiedergabe.
-   Unterstützung für die Bereitstellung von ASF-Streams über ein Netzwerk. Dieses SDK bietet Unterstützung für die Übermittlung von ASF-Daten über HTTP an Remote Computer in einem Netzwerk und auch für die direkte Übermittlung von Daten an einen Windows Media-Remote Server.
-   Unterstützung für das Bearbeiten von Metadaten in ASF-Dateien. Informationen zu einer Datei und deren Inhalt können mit diesem SDK problemlos manipuliert werden. Entwickler können das robuste System der Metadatenattribute verwenden, die im SDK enthalten sind, oder benutzerdefinierte Attribute entsprechend Ihren Anforderungen erstellen.
-   Unterstützung für Inhalts Bearbeitungsanwendungen. Mit diesem SDK können Anwendungen nach Präsentationszeit und Video Frame in einer Datei nach Punkten suchen. Darüber hinaus können mit dem Windows Media-Format-SDK erstellte Dateien Zeitstempel in Formaten verwalten, die in der Film-und Fernsehproduktion verwendet werden.
-   Unterstützung für das Lesen und Bearbeiten von Metadaten in MP3-Dateien. Dieses SDK bietet integrierte Unterstützung für das Lesen von MP3-Dateien mit denselben Methoden, die zum Lesen von ASF-Dateien verwendet werden. Anwendungen, die mit dem Windows Media-Format SDK erstellt wurden, können auch Metadatenattribute in MP3-Dateien mithilfe integrierter Unterstützung der am häufigsten verwendeten ID3-Tags bearbeiten, die von Inhalts Erstellern verwendet werden.
-   Unterstützung für den Schutz von digitalen Rights Management. Dieses SDK bietet Methoden zum Lesen und Schreiben von ASF-Dateien und Netzwerkstreams, die durch digitale Rights Management geschützt sind, um eine unbefugte Wiedergabe oder das Kopieren des Inhalts zu verhindern.

Informationen zum Herunterladen des Windows Media SDK finden Sie auf der Microsoft-Website auf der Seite [Windows Media-Downloads](https://msdn.microsoft.com/windows/desktop/aa904949) .

In diesem Dokument wird beschrieben, wie Sie Anwendungen für digitale Medien mithilfe des SDK für den Windows Media-Format entwickeln können. Es ist in die folgenden Abschnitte unterteilt.

> [!Note]  
> Obwohl dieses Dokument Informationen zur neuesten Version des Windows Media SDK enthält, werden die meisten Features, die es beschreibt, von älteren Versionen des SDK unterstützt. Verweis Seiten für die Methoden, Funktionen, Strukturen und Enumerationen des Windows Media Format SDK enthalten Versions Anforderungen.

 



| `Section`                                                                                                          | BESCHREIBUNG                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum Windows Media-Format-SDK](about-the-windows-media-format-sdk.md)                                     | Enthält eine Übersicht und Hintergrundinformationen, mit denen Sie vertraut sein sollten, bevor Sie versuchen, Anwendungen zu erstellen.                                                                                  |
| [Programmierhandbuch](programming-guide.md)                                                                       | Bietet ausführliche Anweisungen zum Ausführen verschiedener Aufgaben, wie z. b. das Lesen, schreiben und Indizieren von Dateien, das Schützen von Dateien mit digitaler Rights Management, das Streaming von ASF-Daten über ein Netzwerk usw. |
| [Programmierverzeichnis](programming-reference.md)                                                               | Enthält Referenzinformationen zu den Schnittstellen, Methoden, Funktionen, Strukturen, Enumerationstypen und Konstanten im Zusammenhang mit dem Windows Media-Format.                                                     |
| [Windows Media Audio-und Videocodec-Schnittstellen](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Enthält Anweisungen zur direkten Verwendung der Windows Media Audio und Video Codec Digital Media Objects (DMOs).                                                                                           |
| [*Glossar*](wmformat-glossary.md)                                                                              | Definiert die Begriffe, die in der Dokumentation zum Windows Media-Format SDK verwendet werden.                                                                                                                                    |



 

 

 




