---
title: Anwendungswiederherstellung und Neustart
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um eine herunter gefahrene Anwendung automatisch neu zu starten, um ein Update abzuschließen. Speichern von Daten und Konfigurieren der Anwendungs Wiederherstellung vor dem Beenden der Programme.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- Zuverlässigkeit
- Software Zuverlässigkeit
- Anwendungs Wiederherstellung
- Anwendungs Neustart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856803"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="17241-111">Anwendungswiederherstellung und Neustart</span><span class="sxs-lookup"><span data-stu-id="17241-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="17241-112">Zweck</span><span class="sxs-lookup"><span data-stu-id="17241-112">Purpose</span></span>

<span data-ttu-id="17241-113">Eine Anwendung kann die Anwendungs Wiederherstellung und den Neustart (arr) verwenden, um Daten und Zustandsinformationen zu speichern, bevor die Anwendung aufgrund einer nicht behandelten Ausnahme beendet wird, oder wenn die Anwendung nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="17241-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="17241-114">Die Anwendung wird bei Bedarf ebenfalls neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="17241-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="17241-115">Eine Anwendung kann auch neu gestartet werden, wenn ein Installer eine Komponente der Anwendung aktualisiert oder wenn der Computer aufgrund eines Updates neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="17241-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="17241-116">Beachten Sie, dass die Anwendung und das Installationsprogramm entsprechend erstellt werden müssen, um den automatischen Neustart der Anwendung zu unterstützen, nachdem ein Installer eine Anwendung aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="17241-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="17241-117">Weitere Informationen finden Sie unter [registrieren für den Neustart der Anwendung](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="17241-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="17241-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="17241-118">Developer audience</span></span>

<span data-ttu-id="17241-119">ARR ist für C-und C++-Entwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="17241-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="17241-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="17241-120">Run-time requirements</span></span>

<span data-ttu-id="17241-121">ARR ist ab dem Betriebssystem Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17241-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="17241-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="17241-122">In this section</span></span>



| <span data-ttu-id="17241-123">Thema</span><span class="sxs-lookup"><span data-stu-id="17241-123">Topic</span></span>                                                                                                   | <span data-ttu-id="17241-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17241-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="17241-125">Verwenden von Anwendungs Wiederherstellung und Neustart</span><span class="sxs-lookup"><span data-stu-id="17241-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="17241-126">Handbuch für die Registrierung für die Wiederherstellung und den Neustart.</span><span class="sxs-lookup"><span data-stu-id="17241-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="17241-127">Anwendungs Wiederherstellung und Neustart Referenz</span><span class="sxs-lookup"><span data-stu-id="17241-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="17241-128">Referenzinformationen für die ARR-API.</span><span class="sxs-lookup"><span data-stu-id="17241-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





