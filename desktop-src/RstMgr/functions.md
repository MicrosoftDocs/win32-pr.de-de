---
title: Neustart-Manager-Funktionen
description: Die Neustart-Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Neustart-Manager Restart Mgr, Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855967"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="34cd3-104">Neustart-Manager-Funktionen</span><span class="sxs-lookup"><span data-stu-id="34cd3-104">Restart Manager Functions</span></span>

<span data-ttu-id="34cd3-105">Die Neustart-Manager-API verwendet die in der folgenden Tabelle identifizierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="34cd3-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="34cd3-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="34cd3-106">Function</span></span>                                           | <span data-ttu-id="34cd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34cd3-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34cd3-108">**Rmaddfilter**</span><span class="sxs-lookup"><span data-stu-id="34cd3-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="34cd3-109">Ändert das Herunterfahren oder Neustarten von Aktionen.</span><span class="sxs-lookup"><span data-stu-id="34cd3-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="34cd3-110">**Rmstarzession**</span><span class="sxs-lookup"><span data-stu-id="34cd3-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="34cd3-111">Startet eine neue Neustart-Manager-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34cd3-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="34cd3-112">**Rmjoinsession**</span><span class="sxs-lookup"><span data-stu-id="34cd3-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="34cd3-113">Fügt den Prozess einer Anwendung in eine vorhandene Restart Manager-Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="34cd3-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="34cd3-114">**RmEndSession**</span><span class="sxs-lookup"><span data-stu-id="34cd3-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="34cd3-115">Beendet die Neustart-Manager-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34cd3-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="34cd3-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="34cd3-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="34cd3-117">Registriert Ressourcen, z. b. Dateinamen, Dienst Kurznamen [**oder \_ eindeutige \_ RM-Prozess**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) Strukturen, in einer Restart Manager-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34cd3-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="34cd3-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="34cd3-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="34cd3-119">Wird von Installationsprogrammen verwendet, um eine Liste aller von registrierten Ressourcen betroffenen Anwendungen und ihren aktuellen Status zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34cd3-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="34cd3-120">**Rmgetfilterlist**</span><span class="sxs-lookup"><span data-stu-id="34cd3-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="34cd3-121">Fragt den Status des herunter Fahrens und Neustarts von Änderungen ab, die bereits angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="34cd3-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="34cd3-122">**Rmshutdown**</span><span class="sxs-lookup"><span data-stu-id="34cd3-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="34cd3-123">Initiiert das Herunterfahren von Anwendungen und Diensten.</span><span class="sxs-lookup"><span data-stu-id="34cd3-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="34cd3-124">**Rmremovefilter**</span><span class="sxs-lookup"><span data-stu-id="34cd3-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="34cd3-125">Entfernt das Herunterfahren und Neustarten von Änderungen, die bereits angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="34cd3-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="34cd3-126">**Rmrestart**</span><span class="sxs-lookup"><span data-stu-id="34cd3-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="34cd3-127">Startet Anwendungen und Dienste, die durch die [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -Funktion heruntergefahren wurden und für den Neustart registriert wurden, mithilfe von **RegisterApplicationRestart** neu.</span><span class="sxs-lookup"><span data-stu-id="34cd3-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="34cd3-128">**Rmcancelcurrenttask**</span><span class="sxs-lookup"><span data-stu-id="34cd3-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="34cd3-129">Bricht die aktuelle [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)-, [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)-oder [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) -Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="34cd3-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




