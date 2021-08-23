---
title: Erstellen einer Sicherungsanwendung
description: Um Ein- oder Ausgabe auf einem Band durchzuführen, muss eine Sicherungsanwendung zunächst ein Handle des Bandgeräts abrufen. Im folgenden Codebeispiel wird gezeigt, wie Sie die CreateFile-Funktion verwenden, um ein Bandgerät zu öffnen.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Sicherungsanwendungen Sichern
- Erstellen von Sicherungsanwendungen Sichern
- Backup Backup , Erstellen von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086e51bce928b682d3e61518de29118abdc48461a77f79e48a4a4cb4b0f2c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529480"
---
# <a name="creating-a-backup-application"></a>Erstellen einer Sicherungsanwendung

Um Ein- oder Ausgabe auf einem Band durchzuführen, muss eine Sicherungsanwendung zunächst ein Handle des Bandgeräts abrufen. Im folgenden Codebeispiel wird gezeigt, wie Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwenden, um ein Bandgerät zu öffnen.


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



Um eine Verzeichnisstruktur auf einem Band zu sichern, muss eine Anwendung die [**Funktionen FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) und [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) verwenden, um die Verzeichnisstruktur zu durchlaufen. Jedes Mal, wenn eine Datei gefunden wird, sollte die Anwendung die Dateiattribute mithilfe der [**GetFileAttributes-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) erhalten.

Wenn es harte Links gibt, sollte eine Anwendung die Anzahl der Links bestimmen und den eindeutigen Bezeichner der Datei für zukünftige Vergleiche in einer Tabelle speichern. Wenn eine Datei zum ersten Mal gefunden wird, sollte die Anwendung [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwenden, um die Datei zu öffnen, und die [**BackupRead-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-backupread) um die Sicherung zu starten. Anschließend kann die [**WriteFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefile) wiederholt verwendet werden, um alle Informationen im Puffer, die von **BackupRead** verwendet werden, auf das Band zu übertragen. Wenn eine Datei zum zweiten Mal gefunden wird (überprüft auf die Tabelle der Dateibezeichner, wenn harte Links enthalten sind), kann die Anwendung die allgemeinen Dateiinformationen auf das Band schreiben, gefolgt von einem Stream mit einem Bezeichner, der **BACKUP \_ LINK** ist.

Beim Wiederherstellen von Dateien von Band auf Datenträger muss eine Anwendung die [**Funktionen CreateFile,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)und [**ReadFile verwenden.**](/windows/desktop/api/fileapi/nf-fileapi-readfile) Für jede Datei auf einem Band sollte die Anwendung **CreateFile** verwenden, um eine neue Datei auf dem Datenträger zu erstellen, und **BackupWrite,** um mit der Wiederherstellung der Datei zu beginnen. Anschließend sollte die Anwendung **ReadFile** wiederholt verwenden, bis alle Informationen für die Datei vom Band in den Puffer gelesen werden, der von **BackupWrite gefüllt wird.**

Wenn einer der Datenströme im [**BackupWrite-Puffer**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) über einen **BACKUP LINK-Datenstrombezeichner \_** verfügt, muss die Anwendung eine harte Verknüpfung einrichten. Wenn die zum Herstellen des Links erforderlichen Daten nicht vorhanden sind, **schlägt BackupWrite** fehl. Die Anwendung kann einen bereits vorhandenen Katalog verwenden, um die ursprünglichen Daten zu suchen und wiederherzustellen, oder sie kann den Benutzer benachrichtigen, dass sich die wiederherzustellenden Dateidaten an einem anderen Speicherort befinden.

 

 