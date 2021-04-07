---
title: Windows-Remoteverwaltung-Architektur
description: Die Windows-Remoteverwaltung-Architektur besteht aus Komponenten auf den Client-und Server Computern.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729185"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="169d6-103">Windows-Remoteverwaltung-Architektur</span><span class="sxs-lookup"><span data-stu-id="169d6-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="169d6-104">Die Windows-Remoteverwaltung-Architektur besteht aus Komponenten auf den Client-und Server Computern.</span><span class="sxs-lookup"><span data-stu-id="169d6-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="169d6-105">Die folgende Abbildung zeigt die Komponenten auf beiden Computern, die Interaktion der Komponenten mit anderen Komponenten und das Protokoll, das für die Kommunikation zwischen den Computern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="169d6-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![WinRM-Architektur](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="169d6-107">Anfordernder Client</span><span class="sxs-lookup"><span data-stu-id="169d6-107">Requesting Client</span></span>

<span data-ttu-id="169d6-108">Die folgenden WinRM-Komponenten befinden sich auf dem Computer, auf dem das Skript ausgeführt wird, das Daten anfordert.</span><span class="sxs-lookup"><span data-stu-id="169d6-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="169d6-109">WinRM-Anwendung</span><span class="sxs-lookup"><span data-stu-id="169d6-109">WinRM application</span></span>

    <span data-ttu-id="169d6-110">Dies ist das Skript oder **WinRM** -Befehlszeilen Tool, das die WinRM-Skript-API verwendet, um Aufrufe zum Anfordern von Daten oder zum Ausführen von Methoden auszuführen.</span><span class="sxs-lookup"><span data-stu-id="169d6-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="169d6-111">Weitere Informationen finden Sie in der [WinRM-Skript-API](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="169d6-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="169d6-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-112">WSMAuto.dll</span></span>

    <span data-ttu-id="169d6-113">Die Automatisierungs Schicht, die Skriptunterstützung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="169d6-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="169d6-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-114">WsmCL.dll</span></span>

    <span data-ttu-id="169d6-115">C-API-Ebene innerhalb des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="169d6-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="169d6-116">HTTP-API</span><span class="sxs-lookup"><span data-stu-id="169d6-116">HTTP API</span></span>

    <span data-ttu-id="169d6-117">WinRM erfordert Unterstützung für http-und HTTPS-Transport.</span><span class="sxs-lookup"><span data-stu-id="169d6-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="169d6-118">Reaktions Ende Server</span><span class="sxs-lookup"><span data-stu-id="169d6-118">Responding Server</span></span>

<span data-ttu-id="169d6-119">Die folgenden WinRM-Komponenten befinden sich auf dem Reaktions enden Computer.</span><span class="sxs-lookup"><span data-stu-id="169d6-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="169d6-120">HTTP-API</span><span class="sxs-lookup"><span data-stu-id="169d6-120">HTTP API</span></span>

    <span data-ttu-id="169d6-121">WinRM erfordert Unterstützung für http-und HTTPS-Transport.</span><span class="sxs-lookup"><span data-stu-id="169d6-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="169d6-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-122">WSMAuto.dll</span></span>

    <span data-ttu-id="169d6-123">Die Automatisierungs Schicht, die Skriptunterstützung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="169d6-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="169d6-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-124">WsmCL.dll</span></span>

    <span data-ttu-id="169d6-125">C-API-Ebene innerhalb des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="169d6-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="169d6-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-126">WsmSvc.dll</span></span>

    <span data-ttu-id="169d6-127">WinRM- [*Listenerdienst*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="169d6-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="169d6-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-128">WsmProv.dll</span></span>

    <span data-ttu-id="169d6-129">Anbieter Subsystem.</span><span class="sxs-lookup"><span data-stu-id="169d6-129">Provider subsystem.</span></span>

-   <span data-ttu-id="169d6-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-130">WsmRes.dll</span></span>

    <span data-ttu-id="169d6-131">Ressourcendatei</span><span class="sxs-lookup"><span data-stu-id="169d6-131">Resource file.</span></span>

-   <span data-ttu-id="169d6-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="169d6-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="169d6-133">[*WMI-Plug-in*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="169d6-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="169d6-134">Dies ermöglicht Ihnen das Abrufen von WMI-Daten über WinRM.</span><span class="sxs-lookup"><span data-stu-id="169d6-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="169d6-135">Intelligent Platform Management Interface (IPMI)-Treiber und WMI-IPMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="169d6-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="169d6-136">Diese Komponenten stellen alle Hardware Daten bereit, die mithilfe der IPMI-Klassen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="169d6-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="169d6-137">Weitere Informationen finden Sie unter [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="169d6-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="169d6-138">BMC-Hardware muss von dem SMBIOS oder vom Gerät, das manuell erstellt wurde, durch Laden des Treibers erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="169d6-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="169d6-139">Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="169d6-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="169d6-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="169d6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169d6-141">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="169d6-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 