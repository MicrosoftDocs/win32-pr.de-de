---
description: 'Wenn die setupcommitfilequeue-Funktion einen Commit für die Datei Warteschlange ausführt, werden die Datei Vorgänge in der folgenden Reihenfolge verarbeitet: Datei Löschvorgänge, Datei Umbenennungs Vorgänge und schließlich Datei Kopiervorgänge.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Reihenfolge der Warteschlangen Verpflichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865716"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="5ab4f-103">Reihenfolge der Warteschlangen Verpflichtung</span><span class="sxs-lookup"><span data-stu-id="5ab4f-103">Order of Queue Commitment</span></span>

<span data-ttu-id="5ab4f-104">Wenn die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion einen Commit für die Datei Warteschlange ausführt, werden die Datei Vorgänge in der folgenden Reihenfolge verarbeitet: Datei Löschvorgänge, Datei Umbenennungs Vorgänge und schließlich Datei Kopiervorgänge.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="5ab4f-105">Die folgende Gliederung zeigt den Lebenszyklus des Verpflichtungs Prozesses einer Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="5ab4f-106">unter Warteschlange löschen starten</span><span class="sxs-lookup"><span data-stu-id="5ab4f-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="5ab4f-107">Vorgang zum Löschen einer Datei starten <--Wiederholung für jeden</span><span class="sxs-lookup"><span data-stu-id="5ab4f-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="5ab4f-108">beendet einen Datei Löschvorgang < Datei Löschung in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="5ab4f-109">Fertigstellen der unter Warteschlange löschen</span><span class="sxs-lookup"><span data-stu-id="5ab4f-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="5ab4f-110">unter Warteschlange umbenennen starten</span><span class="sxs-lookup"><span data-stu-id="5ab4f-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="5ab4f-111">startet einen Vorgang zum Umbenennen von Dateien <--Wiederholung für jeden</span><span class="sxs-lookup"><span data-stu-id="5ab4f-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="5ab4f-112">beendet einen Datei Löschvorgang < Datei umbenennen in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="5ab4f-113">Schließen Sie die unter Warteschlange Rename</span><span class="sxs-lookup"><span data-stu-id="5ab4f-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="5ab4f-114">Kopieren der subque</span><span class="sxs-lookup"><span data-stu-id="5ab4f-114">start the copy subque</span></span>
    -   <span data-ttu-id="5ab4f-115">Starten eines Datei Kopiervorgangs <--Wiederholung für jeden</span><span class="sxs-lookup"><span data-stu-id="5ab4f-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="5ab4f-116">beendet einen Datei Kopiervorgang < Datei Kopiervorgang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="5ab4f-117">Kopieren der unter Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5ab4f-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="5ab4f-118">Fertigstellen der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5ab4f-118">finish the queue</span></span>

 

<span data-ttu-id="5ab4f-119">Bei jedem Schritt oder wenn ein Fehler auftritt, sendet die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion eine Benachrichtigung an die Rückruf Routine.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="5ab4f-120">Die Rückruf Routine kann die von der Warteschlange gesendeten Informationen verwenden, um den Installationsfortschritt zu verfolgen und ggf. mit dem Benutzer zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="5ab4f-121">Wenn z. b. für einen Datei Kopiervorgang eine Quelldatei erforderlich ist, die im aktuellen Pfad nicht verfügbar war, sendet [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) eine spfilenotify- \_ needmedia-Benachrichtigung an die Rückruf Routine sowie Informationen über die erforderliche Datei und das erforderliche Medium.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="5ab4f-122">Die Rückruf Routine könnte diese Informationen verwenden, um ein Dialogfeld zu generieren, das den Benutzer auffordert, den nächsten Datenträger durch Aufrufen von [ **setuppromptfordisk** einzufügen.](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="5ab4f-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="5ab4f-123">Die Setup-API enthält eine standardmäßige Warteschlangen Rückruf Routine, [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka).</span><span class="sxs-lookup"><span data-stu-id="5ab4f-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="5ab4f-124">Diese Routine verarbeitet Warteschlangen Benachrichtigungen und generiert Fehler Dialogfelder und Status anzeigen für die Installation.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="5ab4f-125">Sie können die standardmäßige Warteschlangen Rückruf Routine verwenden, oder Sie können eine Filter Rückruf Routine schreiben, um eine Teilmenge der Benachrichtigungen zu verarbeiten und die anderen an die standardmäßige Warteschlangen Rückruf Routine zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="5ab4f-126">Wenn keine der Funktionen der Rückruf Routine Ihren Anforderungen entspricht, können Sie eine eigenständige benutzerdefinierte Rückruf Routine schreiben, die nicht die standardmäßige Warteschlangen Rückruf Routine aufruft.</span><span class="sxs-lookup"><span data-stu-id="5ab4f-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="5ab4f-127">Weitere Informationen zu Warteschlangen Rückruf Routinen finden Sie unter [Standard Warteschlangen-Rückruf Routine](default-queue-callback-routine.md)und [Erstellen einer benutzerdefinierten Warteschlangen Rückruf-Routine](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="5ab4f-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



