---
title: Erstellen einer Sicherungs Anwendung
description: Zum Ausführen von Eingaben oder Ausgaben auf einem Band muss eine Sicherungs Anwendung zunächst ein Handle des Bandgeräts abrufen. Im folgenden Codebeispiel wird gezeigt, wie Sie die Funktion "Funktion" zum Öffnen eines Bandgeräts verwenden.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Sicherung von Sicherungs Anwendungen
- Sicherungs Anwendungs Sicherung wird erstellt
- Sicherungs Sicherung, Erstellen von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039360"
---
# <a name="creating-a-backup-application"></a>Erstellen einer Sicherungs Anwendung

Zum Ausführen von Eingaben oder Ausgaben auf einem Band muss eine Sicherungs Anwendung zunächst ein Handle des Bandgeräts abrufen. Im folgenden Codebeispiel wird gezeigt, wie Sie die [**Funktion "Funktion" zum Öffnen**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) eines Bandgeräts verwenden.


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



Zum Sichern einer Verzeichnisstruktur auf einem Band muss eine Anwendung die Funktionen " [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) " verwenden, um die Verzeichnisstruktur zu durchlaufen. Jedes Mal, wenn eine Datei gefunden wird, sollte die Anwendung die Dateiattribute mithilfe der [**getfileattribute**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) -Funktion erhalten.

Wenn feste Links vorhanden sind, sollte eine Anwendung die Anzahl der Verknüpfungen bestimmen und den eindeutigen Bezeichner der Datei in einer Tabelle für künftige Vergleiche speichern. Wenn eine Datei zum ersten Mal gefunden wird, sollte die Anwendung zum Öffnen der Datei die Datei mithilfe von "Anordnungs [**Datei**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " und die [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) -Funktion verwenden, um die Sicherung zu starten. Anschließend kann die Funktion " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " wiederholt verwendet werden, um alle Informationen im Puffer zu übertragen, die von **BackupRead** auf das Band verwendet werden. Beim zweiten Mal, wenn eine Datei gefunden wird (überprüft mit der Tabelle der Datei Bezeichner, wenn es feste Links gibt), kann die Anwendung die allgemeinen Dateiinformationen auf das Band schreiben, gefolgt von einem Stream, der einen Bezeichner mit **Sicherungs \_ Link** aufweist.

Beim Wiederherstellen von Dateien von einem Band auf einen Datenträger muss eine Anwendung die Funktionen " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)", " [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)" und "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " verwenden. Für jede Datei auf einem Band sollte die Anwendung mithilfe von "Create" eine neue Datei **auf dem Daten** Träger **Erstellen und mit** der Wiederherstellung der Datei beginnen. Dann sollte die Anwendung die **Infodatei** wiederholt verwenden, bis alle Informationen für die Datei vom Band in den von **BackupWrite** gefüllten Puffer gelesen werden.

Wenn einer der Streams im [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) -Puffer über einen **\_ sicherungslinkstream** -Bezeichner verfügt, muss die Anwendung einen festen Link einrichten. Wenn die Daten, die zum Herstellen der Verknüpfung erforderlich sind, nicht vorhanden sind, schlägt **BackupWrite** fehl. Die Anwendung kann einen bereits vorhandenen Katalog verwenden, um die ursprünglichen Daten zu suchen und wiederherzustellen, oder Sie kann den Benutzer benachrichtigen, dass sich die wiederherzustellenden Datei Daten an einem anderen Speicherort befinden.

 

 