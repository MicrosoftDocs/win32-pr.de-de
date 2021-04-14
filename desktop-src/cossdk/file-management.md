---
description: Um die Übertragung von Anwendungs Dateien zu ermöglichen, verwaltet Comrepl automatisch Sätze von Dateisystem Ordnern auf Quelle und Ziel. Diese Comrepl-Ordner basieren alle auf der% System dir% \\ com- \\ Replikation.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Dateiverwaltung (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523427"
---
# <a name="file-management"></a><span data-ttu-id="86f3a-104">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="86f3a-104">File Management</span></span>

<span data-ttu-id="86f3a-105">Um die Übertragung von Anwendungs Dateien zu ermöglichen, verwaltet Comrepl automatisch Sätze von Dateisystem Ordnern auf Quelle und Ziel.</span><span class="sxs-lookup"><span data-stu-id="86f3a-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="86f3a-106">Diese Comrepl-Ordner basieren alle auf der% System dir% \\ com- \\ Replikation.</span><span class="sxs-lookup"><span data-stu-id="86f3a-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="86f3a-107">Quellordner</span><span class="sxs-lookup"><span data-stu-id="86f3a-107">Source folders</span></span>



| <span data-ttu-id="86f3a-108">Ordner</span><span class="sxs-lookup"><span data-stu-id="86f3a-108">Folder</span></span>                   | <span data-ttu-id="86f3a-109">Zweck</span><span class="sxs-lookup"><span data-stu-id="86f3a-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f3a-110">Replicasource</span><span class="sxs-lookup"><span data-stu-id="86f3a-110">ReplicaSource</span></span><br/> | <span data-ttu-id="86f3a-111">Anwendungen, die während der Vorbereitungsphase exportiert werden, werden hier gespeichert.</span><span class="sxs-lookup"><span data-stu-id="86f3a-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="86f3a-112">Dieser Ordner wird jedes Mal überschrieben, wenn die Vorbereitungsphase für einen bestimmten Quellcomputer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86f3a-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="86f3a-113">Dieser Ordner wird nie explizit gelöscht, sodass die Replikation an Ziele jederzeit erfolgen kann, nachdem die Quelle vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="86f3a-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="86f3a-114">Jede Anwendung wird in einem eigenen Unterordner mit dem Namen gespeichert <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="86f3a-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="86f3a-115">Zielordner</span><span class="sxs-lookup"><span data-stu-id="86f3a-115">Target folders</span></span>



| <span data-ttu-id="86f3a-116">Ordner</span><span class="sxs-lookup"><span data-stu-id="86f3a-116">Folder</span></span>                    | <span data-ttu-id="86f3a-117">Zweck</span><span class="sxs-lookup"><span data-stu-id="86f3a-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f3a-118">Replikanew</span><span class="sxs-lookup"><span data-stu-id="86f3a-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="86f3a-119">In der Kopier Phase werden alle Dateien und Unterordner von replicasource auf der Quelle in replicanew auf dem Ziel kopiert.</span><span class="sxs-lookup"><span data-stu-id="86f3a-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="86f3a-120">Alle vorherigen Inhalte der replicanew werden immer dann gelöscht, wenn die Kopier Phase für ein bestimmtes Ziel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86f3a-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="86f3a-121">Dieser Ordner ist nur vorhanden, während der Replikationsprozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86f3a-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="86f3a-122">(Siehe replicacurrent.)</span><span class="sxs-lookup"><span data-stu-id="86f3a-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="86f3a-123">Replicacurrent</span><span class="sxs-lookup"><span data-stu-id="86f3a-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="86f3a-124">Die replizierten Anwendungen, die zurzeit auf dem Ziel installiert sind, werden hier gespeichert.</span><span class="sxs-lookup"><span data-stu-id="86f3a-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="86f3a-125">Wenn die Installationsphase gestartet wird, wird der Ordner "replicanew" in "replicacurrent" umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86f3a-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="86f3a-126">Wenn ein vorhandener replicacurrent-Ordner vorhanden ist, wird er in replicaold umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86f3a-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="86f3a-127">Wenn ein vorhandener replicaold-Ordner vorhanden ist, wird der zugehörige Inhalt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86f3a-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="86f3a-128">Replicaold</span><span class="sxs-lookup"><span data-stu-id="86f3a-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="86f3a-129">Speichert die Anwendungs Dateien, die während der nächsten Replikation installiert werden.</span><span class="sxs-lookup"><span data-stu-id="86f3a-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="86f3a-130">Diese Dateien werden nur zu Sicherungszwecken gespeichert.</span><span class="sxs-lookup"><span data-stu-id="86f3a-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="86f3a-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86f3a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f3a-132">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="86f3a-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="86f3a-133">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="86f3a-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="86f3a-134">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="86f3a-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="86f3a-135">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="86f3a-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




