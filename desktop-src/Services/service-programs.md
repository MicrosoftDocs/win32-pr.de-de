---
description: Ein Dienstprogramm enthält ausführbaren Code für einen oder mehrere Dienste.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Dienstprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868187"
---
# <a name="service-programs"></a><span data-ttu-id="99677-103">Dienstprogramme</span><span class="sxs-lookup"><span data-stu-id="99677-103">Service Programs</span></span>

<span data-ttu-id="99677-104">Ein *Dienstprogramm* enthält ausführbaren Code für einen oder mehrere Dienste.</span><span class="sxs-lookup"><span data-stu-id="99677-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="99677-105">Ein Dienstprogramm, das mit dem typdienst Win32-Prozess erstellt wurde, \_ \_ \_ enthält den Code für nur einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="99677-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="99677-106">Ein Dienstprogramm, das mit dem typdienst \_ Win32- \_ Freigabeprozess erstellt wurde \_ , enthält Code für mehr als einen Dienst, der Ihnen die Freigabe von Code ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="99677-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="99677-107">Ein Beispiel für ein Dienstprogramm, das dies tut, ist der generische Dienst Host Prozess, Svchost.exe, der interne Windows-Dienste hostet.</span><span class="sxs-lookup"><span data-stu-id="99677-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="99677-108">Beachten Sie, dass Svchost.exe für die Verwendung durch das Betriebssystem reserviert ist und nicht von nicht-Windows-Diensten verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="99677-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="99677-109">Stattdessen sollten Entwickler eigene Dienst hostingprogramme implementieren.</span><span class="sxs-lookup"><span data-stu-id="99677-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="99677-110">Ein Dienstprogramm kann so konfiguriert werden, dass es im Kontext eines Benutzerkontos entweder über die integrierte (lokale), primäre oder vertrauenswürdige Domäne ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99677-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="99677-111">Sie kann auch so konfiguriert werden, dass Sie in einem speziellen [Dienst Benutzerkonto](service-user-accounts.md)ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99677-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="99677-112">In den folgenden Themen werden die Schnittstellen Anforderungen des [Dienststeuerungs-Managers](service-control-manager.md) (SCM) beschrieben, die ein Dienstprogramm enthalten muss:</span><span class="sxs-lookup"><span data-stu-id="99677-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="99677-113">Dienst Einstiegspunkt</span><span class="sxs-lookup"><span data-stu-id="99677-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="99677-114">ServiceMain-Dienstfunktion</span><span class="sxs-lookup"><span data-stu-id="99677-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="99677-115">Dienststeuerungshandler-Funktion</span><span class="sxs-lookup"><span data-stu-id="99677-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="99677-116">Diese Themen gelten nicht für Treiber Dienste.</span><span class="sxs-lookup"><span data-stu-id="99677-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="99677-117">Informationen zu den Schnittstellen Anforderungen für Treiber Dienste finden Sie im Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="99677-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="99677-118">Ein Dienst wird als Hintergrundprozess ausgeführt, der sich auf die Systemleistung, Reaktionsfähigkeit, Energieeffizienz und Sicherheit auswirkt.</span><span class="sxs-lookup"><span data-stu-id="99677-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="99677-119">Richtlinien zur Dienst Optimierung finden Sie unter [entwickeln effizienter Hintergrundprozesse für Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="99677-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="99677-120">In den folgenden Themen werden zusätzliche Überlegungen zur Programmierung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="99677-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="99677-121">Dienststatus Übergänge</span><span class="sxs-lookup"><span data-stu-id="99677-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="99677-122">Empfangen von Ereignissen in einem Dienst</span><span class="sxs-lookup"><span data-stu-id="99677-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="99677-123">Multithread-Dienste</span><span class="sxs-lookup"><span data-stu-id="99677-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="99677-124">Dienste und die Registrierung</span><span class="sxs-lookup"><span data-stu-id="99677-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="99677-125">Dienste und umgeleitete Laufwerke</span><span class="sxs-lookup"><span data-stu-id="99677-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="99677-126">Dienst Triggerereignisse</span><span class="sxs-lookup"><span data-stu-id="99677-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="99677-127">Beachten Sie Folgendes: Wenn das Dienstprogramm als RPC-Server fungiert, sollte es dynamische Endpunkte und gegenseitige Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="99677-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
