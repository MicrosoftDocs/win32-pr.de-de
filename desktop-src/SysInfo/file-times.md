---
description: Eine Dateizeit ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosekunden-Intervalle darstellt, die seit 12:00 Uhr vergangen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Das System zeichnet Datei Zeiten auf, wenn Anwendungen Dateien erstellen, darauf zugreifen und in Dateien schreiben.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Datei Zeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5919a2378e08798e4cd64d8f8357cb55692bd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869220"
---
# <a name="file-times"></a>Datei Zeiten

Eine *Dateizeit* ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosekunden-Intervalle darstellt, die seit 12:00 Uhr vergangen sind. 1. Januar 1601 koordinierte Weltzeit (UTC). Das System zeichnet Datei Zeiten auf, wenn Anwendungen Dateien erstellen, darauf zugreifen und in Dateien schreiben.

Das NTFS-Dateisystem speichert Zeitwerte im UTC-Format, sodass Sie von Änderungen in der Zeitzone oder der Sommerzeit nicht betroffen sind. Das FAT-Dateisystem speichert Zeitwerte basierend auf der lokalen Zeit des Computers. Beispielsweise wird eine Datei, die am 3.00PM PST in Washington gespeichert wird, als 6:00PM EST in New York auf einem NTFS-Volume angezeigt, aber Sie wird in New York auf einem FAT-Volume als "3:00PM EST" betrachtet.

Zeitstempel werden zu verschiedenen Zeitpunkten und aus verschiedenen Gründen aktualisiert. Die einzige Garantie für einen Datei Zeitstempel ist, dass die Datei Zeit ordnungsgemäß widergespiegelt wird, wenn das Handle, das die Änderung vornimmt, geschlossen wird.

Nicht alle Dateisysteme können Erstellungs-und letzten Zugriffszeiten aufzeichnen, und nicht alle Dateisysteme zeichnen Sie auf die gleiche Weise auf. Beispielsweise beträgt die Auflösung der Erstellungszeit auf FAT 10 Millisekunden, während die Schreibzeit eine Auflösung von 2 Sekunden und die Zugriffszeit eine Auflösung von 1 Tag hat, sodass Sie tatsächlich das Zugriffs Datum ist. Das NTFS-Dateisystem verzögert Updates zum Zeitpunkt des letzten Zugriffs für eine Datei um bis zu einer Stunde nach dem letzten Zugriff.

Verwenden Sie die [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) -Funktion, um die Datei Zeiten für eine angegebene Datei abzurufen. **GetFileTime** kopiert die Erstellungs-, letzten Zugriffs-und letzten Schreibzeiten in einzelne [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Strukturen. Sie können auch Datei Zeiten mithilfe der Funktionen " [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) " abrufen. Diese Funktionen kopieren die Datei Zeiten in **FILETIME** -Strukturen in einer [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Beim Schreiben in eine Datei wird der letzte Schreib Zeitpunkt nicht vollständig aktualisiert, bis alle Handles, die zum Schreiben verwendet werden, geschlossen werden.

Verwenden Sie die [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) -Funktion, um die Datei Zeiten für eine Datei festzulegen. Mit dieser Funktion können Sie die Erstellung, den letzten Zugriff und die letzten Schreibzeiten ändern, ohne den Inhalt der Datei zu ändern. Mit der [**comparefiletime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) -Funktion können Sie die Zeiten verschiedener Dateien vergleichen. Die-Funktion vergleicht zwei Datei Zeiten und gibt einen Wert zurück, der angibt, welcher Zeitpunkt später ist, oder gibt 0 (null) zurück, wenn die Uhrzeiten gleich sind.

Wenn Sie die Datei Zeiten für angegebene Dateien ändern möchten, können Sie ein Datum und eine Uhrzeit in einen dateizeitpunkt konvertieren, indem Sie die [**systemtimedefiletime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) -Funktion verwenden. Sie können auch die Systemzeit in einer [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur abrufen, indem Sie die [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) -Funktion aufrufen.

Verwenden Sie die [**filetimedesystemtime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) -Funktion, damit eine Datei Zeit für Benutzer leicht angezeigt werden kann. **Filetimedesystemtime** konvertiert die Dateizeit und kopiert den Monat, den Tag, das Jahr und die Uhrzeit von der Dateizeit in eine [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur.

## <a name="file-times-and-daylight-saving-time"></a>Datei Zeiten und Sommerzeit

Sie müssen bei der Verwendung von Datei Zeiten darauf achten, dass der Benutzer das System für die automatische Anpassung der Sommerzeit festgelegt hat.

Verwenden Sie die [**filetimetolocalfiletime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) -Funktion, um eine Dateizeit in eine lokale Zeit zu konvertieren. Allerdings verwendet **filetimetolocalfiletime** die aktuellen Einstellungen für die Zeitzone und die Sommerzeit. Wenn es sich um Sommerzeit handelt, ist die Sommerzeit auch dann in Betracht gezogen, wenn die Dateizeit, die Sie umrechnen, normal ist.

Im FAT-Dateisystem werden Zeiten auf dem Datenträger in der Ortszeit aufgezeichnet. [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) ruft zwischengespeicherte UTC-Zeiten aus dem FAT-Dateisystem ab. Wenn es sich um Sommerzeit handelt, liegt die von **GetFileTime** abgerufene Zeit außerhalb einer Stunde, da der Cache nicht aktualisiert wird. Wenn Sie den Computer neu starten, ist die zwischengespeicherte Zeit, die **GetFileTime** abruft, richtig. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) Ruft die Ortszeit aus dem FAT-Dateisystem ab und konvertiert Sie mithilfe der aktuellen Einstellungen für die Zeitzone und die Sommerzeit in die UTC. Wenn es sich um die Sommerzeit handelt, nimmt **FindFirstFile** die Sommerzeit an, selbst wenn die Dateizeit, die Sie umrechnen, normal ist.

Das NTFS-Dateisystem zeichnet Zeiten auf dem Datenträger in UTC auf. Verwenden Sie die folgende Abfolge von Funktionen anstelle von [**filetimetolocalfiletime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime), um die Sommerzeit beim Umrechnen einer Datei Zeit in eine lokale Zeit zu berücksichtigen:

-   [**Filetimeto SYSTEMTIME**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**Systemtimeumtzspecificlocaltime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**Fehler bei SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Datei Zeiten und CDFS

Die Datums-und Zeitstempel von Dateien, die sich auf dem bzw. von einem Medium mithilfe von CDFS (Compact Disk File System) befinden, werden für die lokale Zeitzone angepasst. ISO 9660 gibt an, dass CDFS die Datumsinformationen für die lokale Zeitzone korrekt anzeigen soll. Dies wird dadurch erreicht, dass Datumsangaben für Dateien auf CDFS identisch mit denen im Format Universal Disk Format (UDF) angezeigt werden. UDF ist der neuere Standard für Verteilungs Medien. Wenn Ihr Code von den nicht geänderten Datumsinformationen für eine Datei abhängig ist, die sich in einem oder aus einem Medium mithilfe von CDFS befindet, funktioniert Sie möglicherweise nicht ordnungsgemäß.

 

 
