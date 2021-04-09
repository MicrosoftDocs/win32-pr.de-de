---
description: Glossar der Netzwerkmonitor Begriffe, die mit dem Buchstaben N beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867019"
---
# <a name="n-network-monitor"></a><span data-ttu-id="4249f-103">N (Netzwerkmonitor)</span><span class="sxs-lookup"><span data-stu-id="4249f-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="4249f-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span><span class="sxs-lookup"><span data-stu-id="4249f-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-105">Siehe Netzwerktreiber Schnittstellen Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="4249f-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**Netzwerktreiber Schnittstellen Spezifikation (NDIS)**</span><span class="sxs-lookup"><span data-stu-id="4249f-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-107">Die Spezifikation für die Schnittstelle zwischen Gerätetreibern und einem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4249f-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="4249f-108">Alle Transporte wenden die NDIS-Schnittstelle an, um auf Netzwerkschnittstellenkarten zuzugreifen und Sie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4249f-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Netzwerkmonitor-Agent**</span><span class="sxs-lookup"><span data-stu-id="4249f-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-110">Eine Netzwerkmonitor Komponente.</span><span class="sxs-lookup"><span data-stu-id="4249f-110">A Network Monitor component.</span></span> <span data-ttu-id="4249f-111">Der Agent ermöglicht einem Remote Computer das Erfassen von Daten aus dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4249f-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="4249f-112">Wenn eine Netzwerkmonitor-Installation eine Remote Verbindung mit dem Netzwerkmonitor-Agent herstellt und eine Erfassung initiiert, werden Statistiken aus der Erfassung über das Netzwerk an den Verwaltungs Computer übertragen.</span><span class="sxs-lookup"><span data-stu-id="4249f-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="4249f-113">Die Übertragung wird in den angegebenen Intervallen durchgeführt, wenn die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4249f-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**Netzwerk Paketanbieter (NPP)**</span><span class="sxs-lookup"><span data-stu-id="4249f-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-115">Die Netzwerkmonitor Komponente, die den Netzwerk Datenverkehr in Frames sammelt und die Frames dann an einen Experten, eine NPP-Anwendung, übergibt.</span><span class="sxs-lookup"><span data-stu-id="4249f-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="4249f-116">Ein NPP verwendet den Netzwerkmonitor System Treiber (Nmnt.sys), um die aus dem Netzwerk erfassten Frames zu erhalten, und stellt verschiedene COM-Schnittstellen bereit, die die Frames an eine Anwendung vom Typ "Experte", "Monitor" und "Netzwerk Paketanbieter" übergeben, wo Sie angezeigt und analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="4249f-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span><span class="sxs-lookup"><span data-stu-id="4249f-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-118">Siehe Netzwerk Paketanbieter.</span><span class="sxs-lookup"><span data-stu-id="4249f-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="4249f-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-120">Eine Anwendung, die sowohl die Netzwerkmonitor UI als auch das Überwachungs Steuerungs Tool umgeht und eine direkte Verbindung mit dem Netzwerk Paketanbieter (NPP) herstellt.</span><span class="sxs-lookup"><span data-stu-id="4249f-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="4249f-121">Eine NPP-Anwendung kann mit einer der fünf NPP-com-Schnittstellen eine Verbindung mit der NPP-Komponente herstellen.</span><span class="sxs-lookup"><span data-stu-id="4249f-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="4249f-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP-Finder**</span><span class="sxs-lookup"><span data-stu-id="4249f-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="4249f-123">Die Netzwerkmonitor Komponente, die mit NPPs kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="4249f-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



