---
description: Verwenden von Comrepl
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Verwenden von Comrepl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748640"
---
# <a name="using-comrepl"></a><span data-ttu-id="33b8d-103">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="33b8d-103">Using COMREPL</span></span>

<span data-ttu-id="33b8d-104">Führen Sie die folgenden Schritte aus, um das Befehlszeilen-Hilfsprogramm Comrepl zu starten:</span><span class="sxs-lookup"><span data-stu-id="33b8d-104">To launch the COMREPL command line utility, use the following steps:</span></span>

1.  <span data-ttu-id="33b8d-105">Fügen Sie% windir% \\ system32 \\ com zum Standard Umgebungs Pfad hinzu, indem Sie in der Eingabeaufforderung Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="33b8d-105">Add %windir%\\system32\\Com to the default environment path by typing the following in the command prompt:</span></span>

    <span data-ttu-id="33b8d-106">**Legen Sie path =% path%;% windir% \\ system32 com fest. \\**</span><span class="sxs-lookup"><span data-stu-id="33b8d-106">**set path = %PATH%;%windir%\\system32\\Com**</span></span>

2.  <span data-ttu-id="33b8d-107">Geben Sie den folgenden Comrepl-Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="33b8d-107">Enter the following COMREPL command:</span></span>

    <span data-ttu-id="33b8d-108">**Comrepl** *sourcecomputer* *targetcomputerlist* **\[ /n \[ /v \] \]**</span><span class="sxs-lookup"><span data-stu-id="33b8d-108">**COMREPL** *sourceComputer* *targetComputerList* **\[/n \[/v\]\]**</span></span>

    <span data-ttu-id="33b8d-109">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="33b8d-109">where:</span></span>

    -   <span data-ttu-id="33b8d-110">*sourcecomputer* ist der Computername der Quelle.</span><span class="sxs-lookup"><span data-stu-id="33b8d-110">*sourceComputer* is the computer name of the source</span></span>

    -   <span data-ttu-id="33b8d-111">*targetcomputerlist* ist die Computernamen der Ziele, die durch Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="33b8d-111">*targetComputerList* is the computer names of the targets separated by spaces</span></span>

    -   <span data-ttu-id="33b8d-112">**/n** unterdrückt Bestätigungsaufforderung vor dem Starten der Replikation</span><span class="sxs-lookup"><span data-stu-id="33b8d-112">**/n** suppresses confirmation prompt before starting replication</span></span>

    -   <span data-ttu-id="33b8d-113">**/v** gibt die Protokolldatei Ausgabe an die Konsole aus.</span><span class="sxs-lookup"><span data-stu-id="33b8d-113">**/v** echoes log file output to the console</span></span>

## <a name="notes"></a><span data-ttu-id="33b8d-114">Notizen</span><span class="sxs-lookup"><span data-stu-id="33b8d-114">Notes</span></span>

-   <span data-ttu-id="33b8d-115">Da com+ nicht repliziert wird (nur Konfigurationsdaten und Anwendungen), muss com+ auf allen Ziel Computern bereits installiert sein.</span><span class="sxs-lookup"><span data-stu-id="33b8d-115">Because COM+ is not replicated (only configuration data and applications), all target computers must already have COM+ installed.</span></span>
-   <span data-ttu-id="33b8d-116">Der Benutzer muss sowohl auf dem Quell-als auch auf dem Zielcomputer Rollen Überprüfungen für die Systemanwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="33b8d-116">The user must pass role checks for the system application on both the source and the target computers.</span></span>
-   <span data-ttu-id="33b8d-117">Keine lokalen Computer Konten, die von Rollen verwendet werden können, werden repliziert.</span><span class="sxs-lookup"><span data-stu-id="33b8d-117">No local machine accounts that may be used by roles are replicated.</span></span>
-   <span data-ttu-id="33b8d-118">Der Zielcomputer muss online sein.</span><span class="sxs-lookup"><span data-stu-id="33b8d-118">The target computer(s) must be online.</span></span>
-   <span data-ttu-id="33b8d-119">Der Benutzer ist dafür verantwortlich, alle nicht-com-Daten (z. b. Datenbanktabellen, Datendateien usw.) auf den Ziel Computern zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="33b8d-119">The user is responsible for replicating all non-COM+ data (for example, database tables, data files, and so forth) to the target computer(s).</span></span>
-   <span data-ttu-id="33b8d-120">Cluster können an der Replikation teilnehmen, aber beachten Sie, dass Comrepl nur auf benannte Computer repliziert.</span><span class="sxs-lookup"><span data-stu-id="33b8d-120">Clusters can participate in replication, but note that COMREPL replicates only to named computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33b8d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33b8d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33b8d-122">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="33b8d-122">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="33b8d-123">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="33b8d-123">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="33b8d-124">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="33b8d-124">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="33b8d-125">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="33b8d-125">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



