---
description: Beschreibt, wie Bei der Wiederholung von Punkten das Dateisystemverhalten aktiviert wird, das vom Verhalten abweicht, das die meisten Windows Entwickler erwarten.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Reparse Points and File Operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d18b42c2bc51617e185c2d8f13fde15952ad83d2c2c635d312d589677ee8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015178"
---
# <a name="reparse-points-and-file-operations"></a>Reparse Points and File Operations

*Mithilfe von Wiederholungspunkten* wird das Dateisystemverhalten ermöglicht, das sich von dem Verhalten unterscheidet, das entwickler am meisten Windows Entwickler möglicherweise gewohnt sind. Daher ist es wichtig, diese Verhaltensweisen beim Schreiben von Anwendungen zu kennen, die Dateien bearbeiten, um stabile und zuverlässige Anwendungen zu unterstützen, die auf Dateisysteme zugreifen möchten, die Dies unterstützen. Das Ausmaß dieser Überlegungen hängt von der spezifischen Implementierung und dem zugehörigen Dateisystemfilterverhalten eines bestimmten, benutzerdefinierten Wiederholungspunkts ab. Weitere Informationen finden Sie unter [Reparse Points](reparse-points.md).

Sehen Sie sich die folgenden Beispiele in Bezug auf NTFS-Implementierungen von Wiederholungspunkte an, z. B. bereitgestellte Ordner, verknüpfte Dateien und den Microsoft Remote Storage Server:

-   Sicherungsanwendungen, die [Dateistreams](file-streams.md) verwenden, sollten **BACKUP \_ REPARSE \_ DATA** in der [**WIN32 \_ STREAM \_ ID-Struktur**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) angeben, wenn Dateien mit Auswertungspunkten gesichert werden.
-   Anwendungen, die die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) verwenden, sollten beim Öffnen der Datei das **FLAG FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** angeben, wenn es sich um einen Wiederholungspunkt handelt. Weitere Informationen finden Sie unter [Erstellen und Öffnen von Dateien.](creating-and-opening-files.md)
-   Der Prozess der [Defragmentierung](defragmenting-files.md) von Dateien erfordert eine besondere Behandlung für Dies ist für Dies ist erforderlich.
-   Virenerkennungsanwendungen sollten nach Fehlerpunkten suchen, die verknüpfte Dateien angeben.
-   Die meisten Anwendungen sollten spezielle Aktionen für Dateien ausführen, die in den langfristigen Speicher verschoben wurden, wenn nur der Benutzer darüber informiert wird, dass es eine Weile dauern kann, die Datei abzurufen.
-   Die [**OpenFileById-Funktion**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) öffnet entweder die Datei oder den Wiederholungspunkt, abhängig von der Verwendung des **FLAGS FILE \_ OPEN \_ \_ REPARSE \_ POINT.**
-   Symbolische Verknüpfungen weisen als Wiederholungspunkte bestimmte [spezifische Programmierüberlegungen](symbolic-link-programming-considerations.md) auf.
-   Volumenverwaltungsaktivitäten zum Lesen von Change Journal-Datensätzen der Updatesequenznummer (USN) erfordern eine besondere Behandlung für Dies ist bei Verwendung der [**USN \_ RECORD-**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) und [**READ \_ USN \_ JOURNAL \_ DATA-Strukturen**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bestimmen, ob ein Verzeichnis ein eingebundener Ordner ist](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Erstellen von bereitgestellten Ordnern](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Auswirkungen symbolischer Verknüpfungen auf Dateisystemfunktionen](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
