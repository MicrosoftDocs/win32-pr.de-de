---
description: Eine Dateizeit ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen darstellt, die seit 12:00 Uhr verstrichen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Das System zeichnet Dateizeiten auf, wenn Anwendungen Dateien erstellen, darauf zugreifen und in diese schreiben.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Dateizeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1492597b4e71775974ed8b19f6109c5900a8a28720b769c1c10dcf2f70166b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764492"
---
# <a name="file-times"></a>Dateizeiten

Eine *Dateizeit* ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen darstellt, die seit 12:00 Uhr verstrichen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Das System zeichnet Dateizeiten auf, wenn Anwendungen Dateien erstellen, darauf zugreifen und in diese schreiben.

Das NTFS-Dateisystem speichert Zeitwerte im UTC-Format, sodass sie nicht von Änderungen der Zeitzone oder Sommerzeit betroffen sind. Das FAT-Dateisystem speichert Zeitwerte basierend auf der lokalen Zeit des Computers. Beispielsweise wird eine Datei, die um 15:00 Uhr PST in Washington gespeichert wird, als 18:00 Uhr EST in New York auf einem NTFS-Volume, aber auf einem FAT-Volume als 15:00 Uhr EST in New York angesehen.

Zeitstempel werden zu verschiedenen Zeitpunkten und aus verschiedenen Gründen aktualisiert. Die einzige Garantie für einen Dateizeitstempel ist, dass die Dateizeit richtig reflektiert wird, wenn das Handle, das die Änderung vorsteuert, geschlossen wird.

Nicht alle Dateisysteme können Erstellungs- und letzte Zugriffszeiten aufzeichnen, und nicht alle Dateisysteme zeichnen sie auf die gleiche Weise auf. Beispielsweise beträgt die Auflösung der Erstellungszeit für FAT 10 Millisekunden, während die Schreibzeit eine Auflösung von 2 Sekunden hat und die Zugriffszeit eine Auflösung von 1 Tag hat, sodass es tatsächlich das Zugriffsdatum ist. Das NTFS-Dateisystem verzögert Aktualisierungen der letzten Zugriffszeit für eine Datei um bis zu 1 Stunde nach dem letzten Zugriff.

Verwenden Sie die [**GetFileTime-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) um die Dateizeiten für eine angegebene Datei abzurufen. **GetFileTime kopiert** die Erstellung, den letzten Zugriff und die letzten Schreibzeiten in einzelne [**FILETIME-Strukturen.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Sie können Dateizeiten auch mithilfe der [**Funktionen FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) und [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) abrufen. Diese Funktionen kopieren die Dateizeiten in **FILETIME-Strukturen** in einer [**WIN32 \_ FIND \_ DATA-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Beim Schreiben in eine Datei wird der Zeitpunkt des letzten Schreibzugriffs erst vollständig aktualisiert, wenn alle Handles, die zum Schreiben verwendet werden, geschlossen sind.

Verwenden Sie zum Festlegen der Dateizeiten für eine Datei [**die SetFileTime-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) Mit dieser Funktion können Sie die Erstellung, den letzten Zugriff und die letzten Schreibzeiten ändern, ohne den Inhalt der Datei zu ändern. Sie können die Zeiten verschiedener Dateien mithilfe der [**CompareFileTime-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) vergleichen. Die Funktion vergleicht zwei Dateizeiten und gibt einen Wert zurück, der angibt, welche Zeit später ist, oder gibt 0 (null) zurück, wenn die Zeiten gleich sind.

Wenn Sie die Dateizeiten für angegebene Dateien ändern möchten, können Sie ein Datum und eine Uhrzeit mithilfe der [**SystemTimeToFileTime-Funktion**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) in eine Dateizeit konvertieren. Sie können die Systemzeit auch in einer [**FILETIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) abrufen, indem Sie die [**GetSystemTimeAsFileTime-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) aufrufen.

Verwenden Sie die [**FileTimeToSystemTime-Funktion,**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) um die Anzeige einer Datei für einen Benutzer zu ermöglichen. **FileTimeToSystemTime konvertiert** die Dateizeit und kopiert Monat, Tag, Jahr und Uhrzeit aus der Dateizeit in eine [**SYSTEMTIME-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="file-times-and-daylight-saving-time"></a>Dateizeiten und Sommerzeit

Sie müssen bei der Verwendung von Dateizeiten darauf achten, dass das System automatisch an die Sommerzeit angepasst wird.

Verwenden Sie die [**FileTimeToLocalFileTime-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) um eine Dateizeit in die lokale Zeit zu konvertieren. **FileTimeToLocalFileTime** verwendet jedoch die aktuellen Einstellungen für die Zeitzone und sommerliche Sommerzeit. Wenn es sich also um Sommerzeit handelt, wird die Sommerzeit berücksichtigt, auch wenn die Dateizeit, die Sie konvertieren, in der Standardzeit liegt.

Das FAT-Dateisystem zeichnet Uhrzeiten auf dem Datenträger in Ortszeit auf. [**GetFileTime ruft**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) zwischengespeicherte UTC-Zeiten aus dem FAT-Dateisystem ab. Wenn es zur Sommerzeit wird, ist die von **GetFileTime** abgerufene Zeit eine Stunde nicht mehr, da der Cache nicht aktualisiert wird. Wenn Sie den Computer neu starten, ist die zwischengespeicherte Zeit, die **GetFileTime** abruft, richtig. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) ruft die Ortszeit aus dem FAT-Dateisystem ab und konvertiert sie mithilfe der aktuellen Einstellungen für die Zeitzone und die Sommerzeit in UTC. Wenn es sich um Sommerzeit handelt, berücksichtigt **FindFirstFile** daher die Sommerzeit, auch wenn die Dateizeit, die Sie konvertieren, in der Standardzeit liegt.

Das NTFS-Dateisystem zeichnet die Zeiten auf dem Datenträger in UTC auf. Um die Sommerzeit beim Konvertieren einer Dateizeit in eine lokale Zeit zu berücksichtigen, verwenden Sie die folgende Funktionssequenz, anstatt [**FileTimeToLocalFileTime zu verwenden:**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Dateizeiten und CDFS

Die Datums- und Zeitstempel von Dateien, die sich mithilfe des Compact Disc File System (CDFS) auf Medien befinden oder von diesen stammen, werden für die lokale Zeitzone angepasst. ISO 9660 besagt, dass CDFS die Datumsinformationen ordnungsgemäß für die lokale Zeitzone anzeigen soll. Dies erfolgt so, dass Datumsangaben für Dateien im CDFS mit denen im Universal Disk Format (UDF) angezeigt werden. UdF ist der neuere Standard für Verteilungsmedien. Wenn Ihr Code von den unveränderten Datumsinformationen für eine Datei abhängt, die sich mithilfe von CDFS auf einem Medium befindet oder von diesem stammt, funktioniert er möglicherweise nicht ordnungsgemäß.

 

 
