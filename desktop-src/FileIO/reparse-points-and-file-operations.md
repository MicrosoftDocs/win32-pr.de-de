---
description: Beschreibt, wie Analyse Punkte das Verhalten von Dateisystemen ermöglichen, die von den meisten Windows-Entwicklern erwartet werden.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Analyse Punkte und Datei Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217474"
---
# <a name="reparse-points-and-file-operations"></a>Analyse Punkte und Datei Vorgänge

Analyse *Punkte* ermöglichen das Verhalten des Dateisystems, das von dem Verhalten abweicht, an das die meisten Windows-Entwickler gewöhnt sind. Daher sind diese Verhaltensweisen beim Schreiben von Anwendungen, die Dateien bearbeiten, wichtig für robuste und zuverlässige Anwendungen, die für den Zugriff auf Dateisysteme gedacht sind, die Analyse Punkte unterstützen. Der Umfang dieser Überlegungen hängt von der spezifischen Implementierung und dem zugehörigen Dateisystem Filter Verhalten eines bestimmten Analyse Punkts ab, der Benutzer definiert werden kann. Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md).

Betrachten Sie die folgenden Beispiele für Implementierungen von NTFS-Analyse Punkten, die bereitgestellte Ordner, verknüpfte Dateien und den Microsoft-Remote Speicher Server umfassen:

-   Sicherungs Anwendungen, die [Datei Datenströme](file-streams.md) verwenden, sollten beim Sichern von Dateien mit Analyse Punkten Sicherungs Analysedaten in der Win32- **\_ \_ Daten** [**Strom- \_ \_ ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) -Struktur angeben.
-   Anwendungen, die die Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " verwenden, sollten beim Öffnen der Datei das Flag zum Öffnen des Analyse **\_ \_ \_ \_ Punkts für den Dateiflag** angeben, wenn es sich um einen Analyse Punkt handelt. Weitere Informationen finden Sie unter [Erstellen und Öffnen von Dateien](creating-and-opening-files.md).
-   Für den Prozess der [Defragmentierung von Dateien](defragmenting-files.md) ist eine spezielle Behandlung von Analyse Punkten erforderlich.
-   Viren Erkennungs Anwendungen sollten nach Analyse Punkten suchen, die auf verknüpfte Dateien hinweisen.
-   Die meisten Anwendungen sollten spezielle Aktionen für Dateien durchführen, die in den langfristigen Speicher verschoben wurden, wenn der Benutzer nur benachrichtigt wird, dass es eine Weile dauern kann, bis die Datei abgerufen wird.
-   Die [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) -Funktion öffnet entweder die Datei oder den Analyse Punkt, abhängig von der Verwendung des **\_ Dateiflag zum \_ Öffnen \_ \_** des Analyse Punkts.
-   Symbolische Verknüpfungen, als Analyse Punkte, weisen bestimmte [Programmier Überlegungen](symbolic-link-programming-considerations.md) für Sie auf.
-   Die [**\_ \_ \_ Volumeverwaltungsaktivitäten**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) zum Lesen von Änderungs Journal Datensätzen der Update Sequenznummer (Update Sequence Number, Hern) erfordern eine besondere Behandlung für Analyse Punkte, wenn die Datenstrukturen des Datensatzes und des Daten [**\_ Satzes**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) gelesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Erstellen von bereitgestellten Ordnern](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Symbolische Verknüpfungs Effekte in Dateisystemfunktionen](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
