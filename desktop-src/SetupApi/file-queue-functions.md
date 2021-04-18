---
description: Die folgenden Funktionen werden bei Datei Warteschlangen verwendet.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Datei Warteschlangen Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347475"
---
# <a name="file-queue-functions"></a><span data-ttu-id="e8b84-103">Datei Warteschlangen Funktionen</span><span class="sxs-lookup"><span data-stu-id="e8b84-103">File Queue Functions</span></span>

<span data-ttu-id="e8b84-104">Die folgenden Funktionen werden bei Datei Warteschlangen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8b84-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="e8b84-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="e8b84-105">Function</span></span>                                                             | <span data-ttu-id="e8b84-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8b84-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8b84-107">**Setupclosefilequeue**</span><span class="sxs-lookup"><span data-stu-id="e8b84-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="e8b84-108">Beendet die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e8b84-108">Terminates the queue.</span></span> <span data-ttu-id="e8b84-109">Für alle verbleibenden Transaktionen wird kein Commit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8b84-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="e8b84-110">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="e8b84-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="e8b84-111">Führt einen Commit für alle Transaktionen in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e8b84-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="e8b84-112">**Setupopeinfilequeue**</span><span class="sxs-lookup"><span data-stu-id="e8b84-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="e8b84-113">Initialisiert und gibt ein Handle für die Datei Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="e8b84-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="e8b84-114">**Setuppromptreboot**</span><span class="sxs-lookup"><span data-stu-id="e8b84-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="e8b84-115">Fordert den Benutzer auf, seinen Computer ggf. neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e8b84-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="e8b84-116">**Setupqueuecopy**</span><span class="sxs-lookup"><span data-stu-id="e8b84-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="e8b84-117">Fügt eine Dateikopie in die Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e8b84-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="e8b84-118">**Setupqueuecopysection**</span><span class="sxs-lookup"><span data-stu-id="e8b84-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="e8b84-119">Fügt die Dateien in eine Warteschlange für den INF-Kopiervorgang ein.</span><span class="sxs-lookup"><span data-stu-id="e8b84-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="e8b84-120">**Setupqueuedefaultcopy**</span><span class="sxs-lookup"><span data-stu-id="e8b84-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="e8b84-121">Fügt die Dateien in einer INF-Datei mit den in einer INF-Datei angegebenen Standardinformationen in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="e8b84-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="e8b84-122">**Setupqueuedelete**</span><span class="sxs-lookup"><span data-stu-id="e8b84-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="e8b84-123">Fügt eine Datei Löschung in die Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e8b84-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="e8b84-124">**Setupqueuedeletesection**</span><span class="sxs-lookup"><span data-stu-id="e8b84-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="e8b84-125">Fügt die Dateien in einen INF-Abschnitt zum Löschen von Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e8b84-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="e8b84-126">**Setupqueuerename**</span><span class="sxs-lookup"><span data-stu-id="e8b84-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="e8b84-127">Fügt eine Datei Umbenennung in die Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e8b84-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="e8b84-128">**Setupqueuerenamesection**</span><span class="sxs-lookup"><span data-stu-id="e8b84-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="e8b84-129">Fügt die Dateien in einen INF-Abschnitt zum Umbenennen von Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="e8b84-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="e8b84-130">**Setupscanfilequeue**</span><span class="sxs-lookup"><span data-stu-id="e8b84-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="e8b84-131">Scannt die Datei Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e8b84-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="e8b84-132">**Setupsetplatformpathoverride**</span><span class="sxs-lookup"><span data-stu-id="e8b84-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="e8b84-133">Legt die Platt Form Pfad Überschreibung fest.</span><span class="sxs-lookup"><span data-stu-id="e8b84-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



