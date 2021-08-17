---
description: Ziel der Dateisystemerkennung ist es, dem Windows-Betriebssystem eine zusätzliche Option für ein gültiges, aber nicht unbekanntes Dateisystem zu ermöglichen, das nicht &\# 0034 ist. RAW&\# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Dateisystemerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cf33e8a6e3378ad5b9f0123cb78fa228b5b780e7440a2981b10982e76d187a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996957"
---
# <a name="file-system-recognition"></a>Dateisystemerkennung

Ziel der Dateisystemerkennung ist es, dem Windows-Betriebssystem eine zusätzliche Option für ein gültiges, aber nicht unbekanntes Dateisystem als "RAW" zu ermöglichen. Um dies zu erreichen, definiert das System ab Windows 7 und Windows Server 2008 R2 einen festen Datenstrukturtyp, der auf die Medien geschrieben werden kann, auf denen eine aktivierte Technologie aktiv ist, die das Dateisystemformat ändert. Diese Datenstruktur, wenn sie auf dem sektor 0 (null) des logischen Datenträgers vorhanden ist, wird dann vom Betriebssystem erkannt und informiert den Benutzer, dass das Medium ein gültiges, aber nicht erkanntes Dateisystem enthält und kein RAW-Volume ist, wenn die Treiber für das Dateisystem nicht installiert sind.

## <a name="file-system-recognition-features-and-use"></a>Features und Verwendung der Dateisystemerkennung

Mehrere neuere Speichertechnologien haben das Dateisystemformat auf dem Datenträger so geändert, dass die Medien, auf denen diese Technologien aktiviert sind, für frühere Versionen von Windows nicht mehr erkennbar sind, da die Dateisystemtreiber nicht vorhanden waren, als eine bestimmte frühere Version von Windows veröffentlicht wurde. Das vorherige Standardverhalten in diesem Szenario lautete wie folgt. Wenn es sich bei Speichermedien nicht um ein bekanntes Dateisystem handelt, wird es als RAW identifiziert und dann an die Windows-Shell übermittelt, wo die automatische Wiedergabe mit der Formatbenutzeroberfläche (UI) zur Eingabeaufforderung aufgefordert wird. Die Dateisystemerkennung kann dies lösen, wenn die Autoren des neuen Dateisystems die richtige Datenstruktur ordnungsgemäß auf [**den**](file-system-recognition-structure.md) Datenträger schreiben.

Die Dateisystemerkennung verwendet die folgenden Features und Ebenen innerhalb des Betriebssystems, um ihre Ziele zu erreichen:

-   Storage Medien, bei denen sich eine feste Datenstruktur als Bytefolge befindet, die intern in einer vordefinierten Struktur angeordnet ist, die als [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE-Datenstruktur**](file-system-recognition-structure.md) bezeichnet wird. Es liegt in der Verantwortung des Dateisystementwicklers, diese Struktur auf dem Datenträger ordnungsgemäß zu erstellen.
-   Dateisystemerkennung auf Anwendungsebene, die durch die Verwendung des I/O-Steuerungscodes des [**FSCTL \_ QUERY FILE \_ SYSTEM \_ \_ RECOGNITION-Geräts**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) erreicht wird. Ein Beispiel für die Verwendung dieses Steuerelementcodes finden Sie unter [Abrufen von Informationen zur Dateisystemerkennung.](obtaining-file-system-recognition-information.md)
-   Prüfsummenvalidierungscode, der in der [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE-Datenstruktur**](file-system-recognition-structure.md) gespeichert ist. Ein Beispiel zum Berechnen dieser Prüfsumme finden Sie unter Berechnen einer Prüfsumme für die [Dateisystemerkennung.](computing-a-file-system-recognition-checksum.md)
-   Die Windows Shell-Benutzeroberfläche verwendet die zuvor aufgeführten Features, um flexiblere und stabilere automatische Wiedergabe und zugehörige Unterstützung für unbekannte Dateisysteme zu bieten. Sie kann jedoch nur funktionieren, wenn die FILE [**\_ SYSTEM RECOGNITION \_ \_ STRUCTURE-Datenstruktur**](file-system-recognition-structure.md) im logischen Datenträgersektor 0 vorhanden ist. Entwickler, die neue Dateisysteme implementieren, sollten dieses System verwenden, um sicherzustellen, dass ihr Dateisystem nicht fälschlicherweise vom Typ "RAW" ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Berechnen einer Prüfsumme für die Dateisystemerkennung](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Abrufen von Informationen zur Dateisystemerkennung](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Abrufen von Volumeinformationen](obtaining-volume-information.md)
</dt> </dl>

 

 
