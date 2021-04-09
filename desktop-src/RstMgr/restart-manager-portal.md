---
title: Neustart-Manager
description: Schreiben Sie benutzerdefinierte Installationsprogramme, um Systemneustarts zu vermeiden, die erforderlich sind, um das Aktualisieren einer verwendeten Datei abzuschließen. Herunterfahren und Neustarten aller außer wichtigen Systemdienste von Programmen
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Neustart-Manager neu starten Mgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039327"
---
# <a name="restart-manager"></a><span data-ttu-id="c6d67-105">Neustart-Manager</span><span class="sxs-lookup"><span data-stu-id="c6d67-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="c6d67-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="c6d67-106">Purpose</span></span>

<span data-ttu-id="c6d67-107">Mit der API für den Neustart-Manager können Sie die Anzahl der Systemneustarts, die zum Durchführen einer Installation oder eines Updates erforderlich sind, eliminieren oder verringern.</span><span class="sxs-lookup"><span data-stu-id="c6d67-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="c6d67-108">Der primäre Grund für Software Updates ist ein Systemneustart während einer Installation oder eines Updates erforderlich, da einige der Dateien, die aktualisiert werden, zurzeit von einer ausgelaufenden Anwendung oder einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6d67-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="c6d67-109">Mit dem Neustart-Manager können alle außer den [kritischen System Diensten](critical-system-services.md) heruntergefahren und neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c6d67-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="c6d67-110">Dadurch werden Dateien freigegeben, die verwendet werden, und es können Installations Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6d67-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c6d67-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="c6d67-111">Where applicable</span></span>

<span data-ttu-id="c6d67-112">Die Neustart-Manager-DLL exportiert eine öffentliche C-Schnittstelle, die von standardmäßigen oder benutzerdefinierten Installationsprogrammen geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6d67-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="c6d67-113">Das Installationsprogramm kann den Neustart-Manager zum Registrieren von Dateien verwenden, die während der Installation einer Anwendung oder eines Updates ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6d67-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="c6d67-114">Während einer nachfolgenden Aktualisierung oder Installation kann das Installationsprogramm den Neustart-Manager verwenden, um zu bestimmen, welche Dateien nicht aktualisiert werden können, weil Sie zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6d67-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="c6d67-115">Der Neustart-Manager kann die nicht wichtigen Dienste oder Anwendungen, die diese Dateien zurzeit verwenden, Herunterfahren und neu starten.</span><span class="sxs-lookup"><span data-stu-id="c6d67-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="c6d67-116">Installationsprogramme können den Neustart-Manager anweisen, Anwendungen oder Dienste basierend auf der verwendeten Datei, der Prozess-ID (PID) oder dem Kurznamen eines Windows-Diensts herunterzufahren und neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="c6d67-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="c6d67-117">Der Neustart-Manager ist für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c6d67-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c6d67-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="c6d67-118">Developer audience</span></span>

<span data-ttu-id="c6d67-119">Diese Dokumentation ist für Entwickler von Installationsanwendungen gedacht, die die Installationsfunktionen von Windows Vista oder Windows Server 2008 nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="c6d67-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="c6d67-120">Anwendungen, die die [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4,0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um die Systemneustarts zu verringern.</span><span class="sxs-lookup"><span data-stu-id="c6d67-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="c6d67-121">Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass Sie die Restart Manager-API zum Herunterfahren und Neustarten von Anwendungen und Diensten aufruft.</span><span class="sxs-lookup"><span data-stu-id="c6d67-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="c6d67-122">In Fällen, in denen ein Systemneustart unvermeidlich ist, können Installer die Neustart-Manager-API verwenden, um Neustarts so zu planen, dass die Unterbrechung des Arbeits Flusses des Benutzers minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6d67-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c6d67-123">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="c6d67-123">Run-time requirements</span></span>

<span data-ttu-id="c6d67-124">Die API für den Neustart-Manager ist ab Windows Vista und Windows Server 2008 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6d67-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c6d67-125">Der Neustart-Manager besteht aus einer einzelnen dll, die Anwendungen für den Zugriff auf die Neustart-Manager-API laden können.</span><span class="sxs-lookup"><span data-stu-id="c6d67-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6d67-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c6d67-126">In this section</span></span>



| <span data-ttu-id="c6d67-127">Thema</span><span class="sxs-lookup"><span data-stu-id="c6d67-127">Topic</span></span>                                                                 | <span data-ttu-id="c6d67-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6d67-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="c6d67-129">Informationen zum Neustart-Manager</span><span class="sxs-lookup"><span data-stu-id="c6d67-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="c6d67-130">Übersichts Themen, in denen der Neustart-Manager beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c6d67-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="c6d67-131">Verwenden des Neustart-Managers</span><span class="sxs-lookup"><span data-stu-id="c6d67-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="c6d67-132">Übersichts Themen zur Verwendung der Neustart-Manager-API.</span><span class="sxs-lookup"><span data-stu-id="c6d67-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="c6d67-133">Neustart-Manager-Verweis</span><span class="sxs-lookup"><span data-stu-id="c6d67-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="c6d67-134">Referenz Themen für die Neustart-Manager-API.</span><span class="sxs-lookup"><span data-stu-id="c6d67-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

