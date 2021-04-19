---
description: Comrepl funktioniert in drei Phasen.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Replikations Phasen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346455"
---
# <a name="replication-phases"></a><span data-ttu-id="d205d-103">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="d205d-103">Replication Phases</span></span>

<span data-ttu-id="d205d-104">Comrepl funktioniert in drei Phasen.</span><span class="sxs-lookup"><span data-stu-id="d205d-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="d205d-105">Der Replikationsprozess wird aus den folgenden zwei Gründen in verschiedene Phasen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="d205d-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="d205d-106">So trennen Sie die Arbeit, die für die Vorbereitung der Quelle auf den einzelnen Zielen erledigt ist</span><span class="sxs-lookup"><span data-stu-id="d205d-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="d205d-107">So verzögern Sie die Änderung des Ziels, bis alle Daten aus der Quelle abgerufen wurden</span><span class="sxs-lookup"><span data-stu-id="d205d-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="d205d-108">Die Replikations Phasen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="d205d-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="d205d-109">Phase</span><span class="sxs-lookup"><span data-stu-id="d205d-109">Phase</span></span>         | <span data-ttu-id="d205d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d205d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d205d-111">Vorbereitungsphase</span><span class="sxs-lookup"><span data-stu-id="d205d-111">Prepare phase</span></span> | <span data-ttu-id="d205d-112">Exportiert alle installierten Anwendungen lokal auf den Quellcomputer.</span><span class="sxs-lookup"><span data-stu-id="d205d-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="d205d-113">In dieser Phase wird die Konfiguration von Zielen nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d205d-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d205d-114">Kopier Phase</span><span class="sxs-lookup"><span data-stu-id="d205d-114">Copy phase</span></span>    | <span data-ttu-id="d205d-115">Kopiert Daten auf einen Bereitstellungs Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="d205d-115">Copies data to a target computer.</span></span> <span data-ttu-id="d205d-116">Alle Anwendungen, die auf der Quelle exportiert werden, werden in das Ziel kopiert.</span><span class="sxs-lookup"><span data-stu-id="d205d-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="d205d-117">Dabei handelt es sich um einen Datei Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="d205d-117">This is a file copy operation.</span></span> <span data-ttu-id="d205d-118">(Weitere Informationen finden Sie unter [Dateiverwaltung](file-management.md).) Bei diesem Schritt werden auch einige Daten vom Quellcomputer angefordert, die nicht in exportierten Anwendungs Dateien (z. b. Anwendungs Identitäten) gekapselt sind.</span><span class="sxs-lookup"><span data-stu-id="d205d-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="d205d-119">Diese Daten werden im Arbeitsspeicher in Comrepl gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d205d-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="d205d-120">In dieser Phase wird die Konfiguration von Ziel Computern nicht berührt.</span><span class="sxs-lookup"><span data-stu-id="d205d-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="d205d-121">Installationsphase</span><span class="sxs-lookup"><span data-stu-id="d205d-121">Install phase</span></span> | <span data-ttu-id="d205d-122">Installiert den Quell Katalog auf einem Bereitstellungs Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="d205d-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="d205d-123">Wenn dieser Schritt initiiert wird, befinden sich alle zum Neukonfigurieren des Ziels erforderlichen Daten innerhalb der Anwendungs Dateien im Dateisystem des Ziels oder befinden sich in Comrepl als Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="d205d-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="d205d-124">In dieser Phase werden alle installierten Anwendungen auf dem Ziel gelöscht (außer den in [was replizierten](what-gets-replicated.md)Anwendungen), bevor die aus der Quelle kopierten Anwendungen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d205d-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="d205d-125">Comrepl wird gleichzeitig auf mehreren Zielen installiert, indem ein Installations Thread pro Ziel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d205d-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d205d-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d205d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d205d-127">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="d205d-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="d205d-128">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="d205d-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="d205d-129">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="d205d-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="d205d-130">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="d205d-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



