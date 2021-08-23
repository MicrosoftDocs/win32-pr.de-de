---
title: Bandeingabe und -ausgabe
description: Es gibt mehrere Funktionen, mit denen Anwendungen Eingaben und Ausgaben (E/A) auf einem Bandlaufwerk ausführen können. Band-E/A ähnelt E/A,die auf einem Kommunikationsgerät ausgeführt werden.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Bandeingabe- und -ausgabesicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021269"
---
# <a name="tape-input-and-output"></a>Bandeingabe und -ausgabe

Es gibt mehrere Funktionen, mit denen Anwendungen Eingaben und Ausgaben (E/A) auf einem Bandlaufwerk ausführen können. Band-E/A ähnelt E/A,die auf einem Kommunikationsgerät ausgeführt werden.

Beim Ausführen von Band-E/A speichern einige Bandlaufwerke Informationen zur Bandfirmware in den ersten Blöcken auf einem Band. In der Regel wird ein Teil der ersten 100 Blöcke verwendet. Anwendungen sollten diese Blöcke nicht verwenden. Spezifischere Informationen zu diesem Thema sind von einzelnen Bandsystemherstellern verfügbar. Im Allgemeinen vermeidet eine Anwendung, die die ersten 100 Blöcke auf einem Band überspringt, Bandlaufwerk-Idiosyncrasen.

Die [**Funktionen GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) und [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) rufen die aktuelle Bandposition ab und verschieben sie. Die [**WriteTapemark-Funktion**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) schreibt eine angegebene Anzahl von Setmarks, Dateimarks, kurzen Dateimarks und langen Dateimarks. Die [**EraseTape-Funktion**](/windows/desktop/api/Winbase/nf-winbase-erasetape) löscht ein Band ganz oder teilweise.

Die [**Funktionen ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) lesen und schreiben Dateidaten von und auf das Band. Die Daten werden in vollständigen Blöcken gelesen und geschrieben. Wenn die Blockgröße des Bandes 512 Bytes beträgt, müssen alle Lese- und Schreibvorgänge Puffer verwenden, die einfache ganzzahlige Vielfache dieser Blockgröße sind: 512, 1024, 1536, 2048 und so weiter. Die meisten Laufwerke, wenn nicht alle, lassen nur einen Schreibvorgang zu, nachdem das Band neu gewoben wurde oder nachdem ein Lesevorgang eine Fehlermeldung vom Datentyp "Datenende" erzeugt hat.

Führen Sie zum Lesen oder Schreiben von Dateidaten auf ein bzw. von einem Band im Blockmodus variabler Länge die folgenden Schritte aus:

1.  Bestimmen Sie, ob das Bandlaufwerk den Blockmodus variabler Länge unterstützt, indem Sie die [**GetTapeParameters-Funktion**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) aufrufen und das TAPE DRIVE VARIABLE BLOCK-Bit des \_ \_ \_ **FeaturesLow-Mitglieds** der zurückgegebenen [**TAPE GET DRIVE \_ \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) überprüfen.
2.  Geben Sie den Variablenblockgrößenmodus an, indem Sie die [**Funktion SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) aufrufen und das **BlockSize-Member** der [**TAPE SET MEDIA \_ \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) auf 0 (null) festlegen. Verwenden Sie dann [**ReadFile oder**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) um die Dateidaten zu lesen oder zu schreiben.

Wenn [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) auf ein Dateizeichen trifft, werden die Daten bis zum Dateimark gelesen, und die Funktion schlägt fehl. (Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehlercode zurück, der den Typ des gefundenen Dateizeichens angibt.) Das Betriebssystem verschiebt das Band über das Dateizeichen hinaus, und eine Anwendung kann **ReadFile** erneut aufrufen, um mit dem Lesen fortzufahren.

[**ReadFile und**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile lesen**](/windows/desktop/api/fileapi/nf-fileapi-writefile) und schreiben nur den Datenstrom. Die [**BackupRead-**](/windows/desktop/api/Winbase/nf-winbase-backupread) und [**BackupWrite-Funktionen**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) lesen und schreiben alle Streams, die einer Datei zugeordnet sind. Dazu gehören Daten, erweiterte Attribute, Sicherheit und alternative Datenströme. Die Sicherheitsdatenströme und alternativen Datenströme sind nur für die NTFS-Dateisystempartition relevant.

Die [**BackupSeek-Funktion**](/windows/desktop/api/Winbase/nf-winbase-backupseek) sucht in einer Datei vorwärts, auf die anfänglich [**über BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) oder [**BackupWrite zugegriffen wird.**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) Mit dieser Funktion kann eine Anwendung Informationen überspringen, die Zugriffsfehler verursachen.

Wenn eine Anwendung nur auf die Dateidaten zugreifen muss, sollte sie [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) und [**WriteFile verwenden.**](/windows/desktop/api/fileapi/nf-fileapi-writefile) Diese Funktionen können auch alternative Datenströme lesen, wenn die Datenströme mithilfe der [**CreateFile-Funktion erstellt**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) wurden.

Eine Bandsicherungsanwendung muss [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) und [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) verwenden, um alle Informationen zu einer Datei zu kopieren. Diese Funktionen lesen oder schreiben jedoch keine Dateimerkmale wie Attribute, Dateierstellungszeit und so weiter. Anwendungen müssen die Dateieingabe- und -ausgabefunktionen wie [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) und [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa)verwenden, um diese Werte abzurufen und fest zu legen.

 

 