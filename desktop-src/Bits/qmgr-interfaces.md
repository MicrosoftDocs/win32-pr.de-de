---
title: Qmgr-Schnittstellen
description: Verwenden Sie die folgenden qmgr-Schnittstellen (Queue Manager), um Dateien herunterzuladen und Aufträge in der Download Warteschlange zu überwachen
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206301"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="2215d-103">Qmgr-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2215d-103">QMGR Interfaces</span></span>

<span data-ttu-id="2215d-104">\[Queue Manager-Schnittstellen (qmgr) sind für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen eines Themas angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2215d-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="2215d-105">In nachfolgenden Versionen wurde sie möglicherweise geändert oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="2215d-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2215d-106">Verwenden Sie stattdessen die [Bits-Schnittstellen](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="2215d-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="2215d-107">Verwenden Sie die folgenden qmgr-Schnittstellen (Queue Manager), um Dateien herunterzuladen und Aufträge in der Download Warteschlange zu überwachen</span><span class="sxs-lookup"><span data-stu-id="2215d-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="2215d-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2215d-108">Interface</span></span>                                                                 | <span data-ttu-id="2215d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2215d-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2215d-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="2215d-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="2215d-111">Implementieren Sie, um Benachrichtigungen zu empfangen, wenn Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="2215d-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2215d-112">**Ibackgroundcopygroup**</span><span class="sxs-lookup"><span data-stu-id="2215d-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="2215d-113">Verwenden Sie, um die Gruppe zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2215d-113">Use to manage the group.</span></span> <span data-ttu-id="2215d-114">Fügen Sie z. b. der Gruppe einen Auftrag hinzu, legen Sie die Eigenschaften der Gruppe fest, und starten und starten Sie die Gruppe in der Download Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2215d-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="2215d-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="2215d-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="2215d-116">Verwenden Sie, um dem Auftrag Dateien hinzuzufügen und den Status des Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2215d-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2215d-117">**Ibackgroundcopyqmgr**</span><span class="sxs-lookup"><span data-stu-id="2215d-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="2215d-118">Verwenden Sie, um eine neue Gruppe zu erstellen, eine vorhandene Gruppe abzurufen oder alle Gruppen in der Warteschlange aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="2215d-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="2215d-119">**Ienumbackgroundcopygroups**</span><span class="sxs-lookup"><span data-stu-id="2215d-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="2215d-120">Verwenden Sie, um eine Liste der Gruppen in der Download Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2215d-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2215d-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="2215d-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="2215d-122">Verwenden Sie, um eine Liste der Aufträge in der Gruppe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2215d-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





