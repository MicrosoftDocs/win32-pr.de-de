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
# <a name="creating-a-backup-application"></a><span data-ttu-id="4df65-107">Erstellen einer Sicherungs Anwendung</span><span class="sxs-lookup"><span data-stu-id="4df65-107">Creating a Backup Application</span></span>

<span data-ttu-id="4df65-108">Zum Ausführen von Eingaben oder Ausgaben auf einem Band muss eine Sicherungs Anwendung zunächst ein Handle des Bandgeräts abrufen.</span><span class="sxs-lookup"><span data-stu-id="4df65-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="4df65-109">Im folgenden Codebeispiel wird gezeigt, wie Sie die [**Funktion "Funktion" zum Öffnen**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) eines Bandgeräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="4df65-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


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



<span data-ttu-id="4df65-110">Zum Sichern einer Verzeichnisstruktur auf einem Band muss eine Anwendung die Funktionen " [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) " und " [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) " verwenden, um die Verzeichnisstruktur zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4df65-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="4df65-111">Jedes Mal, wenn eine Datei gefunden wird, sollte die Anwendung die Dateiattribute mithilfe der [**getfileattribute**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) -Funktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="4df65-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="4df65-112">Wenn feste Links vorhanden sind, sollte eine Anwendung die Anzahl der Verknüpfungen bestimmen und den eindeutigen Bezeichner der Datei in einer Tabelle für künftige Vergleiche speichern.</span><span class="sxs-lookup"><span data-stu-id="4df65-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="4df65-113">Wenn eine Datei zum ersten Mal gefunden wird, sollte die Anwendung zum Öffnen der Datei die Datei mithilfe von "Anordnungs [**Datei**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " und die [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) -Funktion verwenden, um die Sicherung zu starten.</span><span class="sxs-lookup"><span data-stu-id="4df65-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="4df65-114">Anschließend kann die Funktion " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " wiederholt verwendet werden, um alle Informationen im Puffer zu übertragen, die von **BackupRead** auf das Band verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4df65-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="4df65-115">Beim zweiten Mal, wenn eine Datei gefunden wird (überprüft mit der Tabelle der Datei Bezeichner, wenn es feste Links gibt), kann die Anwendung die allgemeinen Dateiinformationen auf das Band schreiben, gefolgt von einem Stream, der einen Bezeichner mit **Sicherungs \_ Link** aufweist.</span><span class="sxs-lookup"><span data-stu-id="4df65-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="4df65-116">Beim Wiederherstellen von Dateien von einem Band auf einen Datenträger muss eine Anwendung die Funktionen " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)", " [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)" und "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="4df65-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="4df65-117">Für jede Datei auf einem Band sollte die Anwendung mithilfe von "Create" eine neue Datei **auf dem Daten** Träger **Erstellen und mit** der Wiederherstellung der Datei beginnen.</span><span class="sxs-lookup"><span data-stu-id="4df65-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="4df65-118">Dann sollte die Anwendung die **Infodatei** wiederholt verwenden, bis alle Informationen für die Datei vom Band in den von **BackupWrite** gefüllten Puffer gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="4df65-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="4df65-119">Wenn einer der Streams im [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) -Puffer über einen **\_ sicherungslinkstream** -Bezeichner verfügt, muss die Anwendung einen festen Link einrichten.</span><span class="sxs-lookup"><span data-stu-id="4df65-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="4df65-120">Wenn die Daten, die zum Herstellen der Verknüpfung erforderlich sind, nicht vorhanden sind, schlägt **BackupWrite** fehl.</span><span class="sxs-lookup"><span data-stu-id="4df65-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="4df65-121">Die Anwendung kann einen bereits vorhandenen Katalog verwenden, um die ursprünglichen Daten zu suchen und wiederherzustellen, oder Sie kann den Benutzer benachrichtigen, dass sich die wiederherzustellenden Datei Daten an einem anderen Speicherort befinden.</span><span class="sxs-lookup"><span data-stu-id="4df65-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 