---
description: Der WMI-Anbieter für Hyper-V ermöglicht Entwicklern und skriskriptern, schnell benutzerdefinierte Tools, Hilfsprogramme und Erweiterungen für die Virtualisierungsplattform zu erstellen. Die WMI-Schnittstellen können alle Aspekte der Hyper-V-Dienste verwalten.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: Informationen zum Hyper-V-WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350236"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="7c22c-104">Informationen zum Hyper-V-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7c22c-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="7c22c-105">Der WMI-Anbieter für Hyper-V ermöglicht Entwicklern und skriskriptern, schnell benutzerdefinierte Tools, Hilfsprogramme und Erweiterungen für die Virtualisierungsplattform zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c22c-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="7c22c-106">Die WMI-Schnittstellen können alle Aspekte der Hyper-V-Dienste verwalten.</span><span class="sxs-lookup"><span data-stu-id="7c22c-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="7c22c-107">Informationen zu Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="7c22c-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="7c22c-108">Microsoft Windows Server 2008 R2 Hyper-V ermöglicht es Systemadministratoren, separate Hardware Server auf einem einzelnen Server, auf dem Microsoft Windows Server 2008 R2 ausgeführt wird, als Host Betriebssystem zu konsolidieren.</span><span class="sxs-lookup"><span data-stu-id="7c22c-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="7c22c-109">Alle gehosteten virtuellen Computer werden in einer eigenen separaten und isolierten virtuellen Umgebung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c22c-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="7c22c-110">Dies ermöglicht es dem Administrator, eine einfache Verwaltung, Bereitstellung und Verwaltung einer großen Anzahl von virtuellen Computern zu ermöglichen und gleichzeitig das Ausführen mehrerer Hardwarelösungen für die Verwendung verschiedener Produkte und Betriebssysteme zu verringern.</span><span class="sxs-lookup"><span data-stu-id="7c22c-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="7c22c-111">Ein weiterer Vorteil der virtuellen Computerumgebung besteht im Testen und unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c22c-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="7c22c-112">Neue Server-und Systemkonfigurationen können parallel zum vorhandenen System bereitgestellt und getestet werden, ohne dass während der Rollout Phase aufwändige Ausfallzeiten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c22c-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="7c22c-113">Jeder virtuelle Computer kann so eingerichtet werden, dass unterschiedliche Konfigurationen bei Ausführung auf einer Standardplattform verwendet werden, um bessere Testergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="7c22c-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="7c22c-114">Mit der Unterstützung für ältere Betriebssysteme können ältere Hardware, Systeme und Anwendungen unterstützt und getestet werden.</span><span class="sxs-lookup"><span data-stu-id="7c22c-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="7c22c-115">Mithilfe der momentaufnahmenunterstützung können Sie eine Momentaufnahme des Zustands einer virtuellen Maschine erstellen, damit Sie bei Bedarf zu einem vorherigen Ereignis zurückkehren können.</span><span class="sxs-lookup"><span data-stu-id="7c22c-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="7c22c-116">Hyper-V stellt eine umfangreiche Oberfläche zur Verfügung, mit der der Benutzer die virtuelle Computerumgebung überwachen und steuern können.</span><span class="sxs-lookup"><span data-stu-id="7c22c-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="7c22c-117">Die meisten Hyper-V-Geräte können mithilfe des WMI-Anbieters gesteuert werden, was eine einfache und dennoch leistungsfähige Anpassung der virtuellen Computer ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7c22c-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="7c22c-118">Weitere Informationen zu den Möglichkeiten, die mit dem WMI-Anbieter gesteuert werden können, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7c22c-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="7c22c-119">Verwaltungsdienst für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="7c22c-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="7c22c-120">Netzwerkdienst</span><span class="sxs-lookup"><span data-stu-id="7c22c-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="7c22c-121">Ressourcen Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="7c22c-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="7c22c-122">Neues in Hyper-V-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7c22c-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



