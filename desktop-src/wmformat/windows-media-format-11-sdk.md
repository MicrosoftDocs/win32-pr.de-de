---
title: Windows Medienformat 11 SDK
description: Windows Medienformat 11 SDK
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Medienformat-SDK, Informationen
- Windows Medien-SDK
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Informationen
- ASF (Advanced Systems Format), Informationen
- Windows Medienformat-SDK, Features
- Windows Medienformat-SDK, wichtige Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70af68402ea5a22a9499ca09fd4b2e4022f304ee5ebf68a4f877a978ad168e4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839430"
---
# <a name="windows-media-format-11-sdk"></a>Windows Medienformat 11 SDK

Diese Dokumentation beschreibt das Microsoft Windows Media Format Software Development Kit (SDK) und gilt für die 32-Bit- und x64-basierten Versionen des SDK.

Das Windows Media Format SDK ist eine Komponente des Microsoft Windows Media Software Development Kit (SDK). Weitere Komponenten sind Windows Media-Dienste SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK, Windows Media Geräte-Manager SDK und Windows Media Player SDK.

Das Windows Media Format SDK bietet Anwendungsentwicklern Zugriff auf die Komponenten des Windows Medienformats. Zu diesen Komponenten gehören der ASF-Dateicontainer (Advanced Systems Format), die Windows-Codecs für Medienaudio und -video, die grundlegende Netzwerkstreamingfunktion und die Verwaltung digitaler Rechte. Die Objekte des Windows Media Format SDK bearbeiten die Komponenten Windows Medien auf niedriger Ebene. Die anderen Komponenten des Windows Media SDK enthalten Objekte, die auf einer höheren Ebene funktionieren.

Der Hauptzweck des Windows Media Format SDK besteht in der Erstellung von Anwendungen, die ASF-Dateien (Advanced Systems Format) und Netzwerkstreams wieder geben, schreiben, bearbeiten, verschlüsseln und liefern. Diese Dateien und Streams enthalten in der Regel Audio- und Videoinhalte, die mithilfe der Windows-Codecs für Medienaudio und Video codiert wurden. ASF kann jedoch beliebige Datentypen enthalten. Weitere Informationen zur Containerstruktur "Advanced Systems Format" finden Sie unter [Übersicht über das ASF-Format.](overview-of-the-asf-format.md)

Die wichtigsten Features des Windows Media Format SDK sind:

-   Unterstützung branchenführender Codecs. Das Windows Media Format 11 SDK enthält den Microsoft Windows Media Video 9-Codec und den Microsoft Windows Media Audio 9.1-Codec. Beide Codecs bieten eine besondere Codierung digitaler Medieninhalte. Neu für dieses Release ist der Windows Media Video 9 Advanced Profile-Codec, der Optimierungen für die Videoübertragung bietet. Dieses SDK enthält auch den Microsoft Windows Media Video 9 Screen-Codec zum Komprimieren von Computerbildschirmaktivitäten während Sitzungen von Benutzeranwendungen und den Windows Media Audio 9.1 Voice-Codec, der Audio mit geringer Komplexität codiert, z. B. Sprache, und sich intelligent an komplexere Audioinhalte wie Musik anpasst, um kombinierte Stimm-Musik-Szenarien besser zu machen.
-   Unterstützung für das Schreiben von ASF-Dateien. Dateien werden basierend auf anpassbaren Profilen erstellt und ermöglichen eine einfache Konfiguration und Standardisierung von Dateien. Dieses SDK kann verwendet werden, um Dateien mit mehr als 2 Gigabyte zu schreiben, wodurch längere dateien mit besserer Qualität und fortlaufender Qualität erstellt werden können.
-   Unterstützung für das Lesen von ASF-Dateien. Dieses SDK bietet Unterstützung für das Lesen lokaler ASF-Dateien sowie das Lesen von ASF-Daten, die über ein Netzwerk gestreamt werden. Unterstützung wird auch für viele erweiterte Lesefunktionen bereitgestellt, z. B. native Unterstützung für MBR-Dateien (Multiple Bit Rate), die mehrere Streams mit demselben Inhalt enthalten, der mit unterschiedlichen Bitraten codiert ist. Der Reader wählt je nach verfügbarer Bandbreite zum Zeitpunkt der Wiedergabe automatisch aus, welcher MBR-Stream verwendet werden soll.
-   Unterstützung für die Bereitstellung von ASF-Streams über ein Netzwerk. Dieses SDK bietet Unterstützung für die Bereitstellung von ASF-Daten über HTTP an Remotecomputer in einem Netzwerk sowie für die direkte Bereitstellung von Daten an einen remote Windows Media-Server.
-   Unterstützung für das Bearbeiten von Metadaten in ASF-Dateien. Informationen zu einer Datei und ihrem Inhalt können mit diesem SDK leicht bearbeitet werden. Entwickler können das robuste System von Metadatenattributen verwenden, die im SDK enthalten sind, oder benutzerdefinierte Attribute erstellen, um ihre Anforderungen zu erfüllen.
-   Unterstützung für Inhaltsbearbeitungsanwendungen. Mit diesem SDK können Anwendungen nach Punkten innerhalb einer Datei suchen, indem die Präsentationszeit und der Videoframe verwendet werden. Darüber hinaus können Dateien, die mit dem Windows Media Format SDK erstellt wurden, Zeitstempel in Formaten verwalten, die in der Film- und Fernsehproduktion verwendet werden.
-   Unterstützung für das Lesen und Bearbeiten von Metadaten in MP3-Dateien. Dieses SDK bietet integrierte Unterstützung für das Lesen von MP3-Dateien mit den gleichen Methoden, die zum Lesen von ASF-Dateien verwendet werden. Anwendungen, die mit dem Windows Media Format SDK erstellt wurden, können Metadatenattribute in MP3-Dateien auch mithilfe der integrierten Unterstützung für die gängigsten ID3-Tags bearbeiten, die von Inhaltserstellern verwendet werden.
-   Unterstützung für digital Rights Management Schutz. Dieses SDK stellt Methoden zum Lesen und Schreiben von ASF-Dateien und Netzwerkstreams bereit, die durch Digital Rights Management geschützt sind, um eine nicht autorisierte Wiedergabe oder Kopie des Inhalts zu verhindern.

Informationen zum Herunterladen des Windows Media Format [](https://msdn.microsoft.com/windows/desktop/aa904949) SDK finden Sie auf Windows Microsoft-Website auf der Seite Mediendownloads.

In diesem Dokument wird beschrieben, wie Sie digitale Medienanwendungen mit dem Windows Media Format SDK entwickeln können. Sie ist in die folgenden Abschnitte unterteilt.

> [!Note]  
> Obwohl dieses Dokument Informationen über die neueste Version des Windows Media Format SDK enthält, werden die meisten der beschriebenen Features von älteren Versionen des SDK unterstützt. Referenzseiten für die Methoden, Funktionen, Strukturen und Enumerationen des Windows Media Format SDK enthalten Versionsanforderungen.

 



| `Section`                                                                                                          | BESCHREIBUNG                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum Windows Media Format SDK](about-the-windows-media-format-sdk.md)                                     | Enthält Übersichts- und Hintergrundinformationen, mit denen Sie vertraut sein sollten, bevor Sie versuchen, Anwendungen zu erstellen.                                                                                  |
| [Programmierhandbuch](programming-guide.md)                                                                       | Enthält ausführliche Anweisungen zum Ausführen verschiedener Aufgaben, z. B. Lesen, Schreiben und Indizieren von Dateien, Schützen von Dateien mit Digital Rights Management, Streamen von ASF-Daten über ein Netzwerk und so weiter. |
| [Programmierverzeichnis](programming-reference.md)                                                               | Stellt Referenzinformationen für die Schnittstellen, Methoden, Funktionen, Strukturen, Enumerationstypen und Konstanten bereit, die sich auf Windows Medienformats bezieht.                                                     |
| [Windows Medienaudio- und Videocodecschnittstellen](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Enthält Anweisungen für die direkte Windows medienaudio- und videocodec-Objekte (Digital Media Objects, DMOs).                                                                                           |
| [*Glossar*](wmformat-glossary.md)                                                                              | Definiert die Begriffe, die in der Dokumentation Windows Media Format SDK verwendet werden.                                                                                                                                    |



 

 

 




