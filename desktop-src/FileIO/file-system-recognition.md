---
description: Das Ziel der Dateisystem Erkennung besteht darin, dem Windows-Betriebssystem eine zusätzliche Option für ein gültiges, aber nicht erkanntes Dateisystem zu ermöglichen, das nicht &\# 0034; RAW&\# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Datei System Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347898"
---
# <a name="file-system-recognition"></a>Datei System Erkennung

Das Ziel der Dateisystem Erkennung besteht darin, dass das Windows-Betriebssystem über eine zusätzliche Option für ein gültiges, aber unbekanntes Dateisystem als "RAW" verfügt. Um dies zu erreichen, definiert das System ab Windows 7 und Windows Server 2008 R2 einen festgelegten Daten Strukturtyp, der auf das Medium geschrieben werden kann, auf dem eine aktivierte Technologie, die das Dateisystem Format ändert, aktiv ist. Diese Datenstruktur, falls Sie auf dem logischen Datenträger Sektor 0 (null) vorhanden ist, wird dann vom Betriebssystem erkannt, und der Benutzer wird benachrichtigt, dass die Medien ein gültiges, aber unbekanntes Dateisystem enthalten, das kein Rohdaten Volume ist, wenn die Treiber für das Dateisystem nicht installiert sind.

## <a name="file-system-recognition-features-and-use"></a>Features und Verwendung von Datei System Erkennungsfunktionen

Mehrere aktuelle Speichertechnologien haben das Dateisystem Format auf dem Datenträger geändert, sodass die Medien, auf denen diese Technologien aktiviert sind, in früheren Versionen von Windows nicht erkannt werden können, weil die Dateisystem Treiber nicht vorhanden waren, als eine bestimmte frühere Windows-Version veröffentlicht wurde. Das vorherige Standardverhalten in diesem Szenario lautete wie folgt: Wenn es sich bei Speichermedien nicht um ein bekanntes Dateisystem handelt, wird es als RAW identifiziert und dann an die Windows-Shell weitergegeben, in der die Eingabeaufforderung mit dem Format Benutzeroberfläche (UI) angezeigt wird. Die Dateisystem Erkennung kann diese Lösung beheben, wenn die Autoren des neuen Dateisystems die richtige [**Datenstruktur**](file-system-recognition-structure.md) ordnungsgemäß auf den Datenträger schreiben.

Die Dateisystem Erkennung verwendet die folgenden Features und Ebenen innerhalb des Betriebssystems, um die Ziele zu erreichen:

-   Speichermedien, bei denen eine Datenstruktur mit fester Größe als Bytefolge intern in einer vordefinierten Struktur angeordnet ist, die als [**Datei \_ System- \_ Erkennungs \_ Struktur**](file-system-recognition-structure.md) -Datenstruktur bezeichnet wird. Es liegt in der Verantwortung des Dateisystem Entwicklers, diese Struktur auf dem Datenträger ordnungsgemäß zu erstellen.
-   Dateisystem Erkennung auf Anwendungsebene, die über den e/a-Steuerungs Code des [**FSCTL- \_ Abfrage \_ Datei \_ System \_ Erkennungs**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) Geräts erreicht wurde. Ein Beispiel für die Verwendung dieses Steuerungs Codes finden Sie unter Abrufen von [Informationen zur Datei System Erkennung](obtaining-file-system-recognition-information.md).
-   Prüfsummen-Validierungscode, der in der Datenstruktur der [**Datei \_ System \_ Erkennungs \_ Struktur**](file-system-recognition-structure.md) gespeichert ist. Ein Beispiel für die Berechnung dieser Prüfsumme finden Sie unter Berechnen [einer Prüfsumme für die Datei System Erkennung](computing-a-file-system-recognition-checksum.md).
-   Die Windows-Shellbenutzeroberfläche verwendet die zuvor aufgeführten Features, um eine flexiblere und stabilere AutoPlay und zugehörige Unterstützung für unbekannte Dateisysteme bereitzustellen. Sie kann jedoch nur verwendet werden, wenn die Datenstruktur der [**Datei \_ System \_ Erkennungs \_ Struktur**](file-system-recognition-structure.md) im logischen Datenträger Sektor NULL vorhanden ist. Entwickler, die neue Dateisysteme implementieren, sollten dieses System verwenden, um sicherzustellen, dass das Dateisystem nicht versehentlich den Typ "RAW" annimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Berechnen einer Prüfsumme für die Datei System Erkennung](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Abrufen von Informationen zur Datei System Erkennung](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Abrufen von Volumeinformationen](obtaining-volume-information.md)
</dt> </dl>

 

 
