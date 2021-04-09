---
title: SNMP-Dienst
description: Die Microsoft Windows-Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remote Geräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerk Verwendung zu überwachen und Netzwerkfehler oder nicht geeigneten Zugriff zu erkennen. Wichtig die Microsoft Windows SNMP-API unterstützt nur Protokoll Versionen bis SNMPv2C. Spätere Versionen des Protokolls werden nicht unterstützt.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP-SNMP
- SNMP-SNMP, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039487"
---
# <a name="snmp-service"></a><span data-ttu-id="a4e31-106">SNMP-Dienst</span><span class="sxs-lookup"><span data-stu-id="a4e31-106">SNMP Service</span></span>

<span data-ttu-id="a4e31-107">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a4e31-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4e31-108">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a4e31-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a4e31-109">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="a4e31-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="a4e31-110">Zweck</span><span class="sxs-lookup"><span data-stu-id="a4e31-110">Purpose</span></span>

<span data-ttu-id="a4e31-111">Die Microsoft Windows-Implementierung des Simple Network Management Protocol (SNMP) wird verwendet, um Remote Geräte zu konfigurieren, die Netzwerkleistung zu überwachen, die Netzwerk Verwendung zu überwachen und Netzwerkfehler oder nicht geeigneten Zugriff zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="a4e31-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4e31-112">Die Microsoft Windows SNMP-API unterstützt nur Protokoll Versionen bis SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="a4e31-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="a4e31-113">Spätere Versionen des Protokolls werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4e31-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="a4e31-114">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a4e31-114">Where applicable</span></span>

<span data-ttu-id="a4e31-115">SNMP verwendet eine verteilte Architektur, bestehend aus Verwaltungs Anwendungen und Agent-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a4e31-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="a4e31-116">Der SNMP-Dienst implementiert einen SNMP-Agent.</span><span class="sxs-lookup"><span data-stu-id="a4e31-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="a4e31-117">Um die Informationen zu verwenden, die der SNMP-Dienst bereitstellt, muss mindestens ein Host vorhanden sein, auf dem eine SNMP-Verwaltungs Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4e31-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="a4e31-118">Sie können SNMP-Verwaltungssoftware von Drittanbietern verwenden, oder Sie können eine eigene SNMP-Verwaltungssoftware Anwendung entwickeln.</span><span class="sxs-lookup"><span data-stu-id="a4e31-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="a4e31-119">Zu diesem Zweck stehen die folgenden APIs zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="a4e31-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="a4e31-120">SNMP-Verwaltungs-API, eine Reihe von Funktionen, die verwendet werden können, um schnell einfache SNMP-Verwaltungssysteme zu entwickeln</span><span class="sxs-lookup"><span data-stu-id="a4e31-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="a4e31-121">WinSNMP-API, Version 2,0, eine Reihe von Funktionen zum Codieren, decodieren, senden und empfangen von SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="a4e31-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="a4e31-122">Darüber hinaus definiert die SNMP-Erweiterungs-Agent-API die Schnittstelle zwischen dem SNMP-Dienst und den DLLs des SNMP-Erweiterungs-Agents von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="a4e31-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="a4e31-123">Die API-Funktionen des SNMP-Hilfsprogramms können zur Vereinfachung der Verarbeitung von SNMP-Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4e31-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a4e31-124">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="a4e31-124">Developer audience</span></span>

<span data-ttu-id="a4e31-125">Die im vorherigen Abschnitt aufgeführten APIs sind für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="a4e31-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a4e31-126">Eine Vertrautheit mit SNMP und SNMPv2C sowie ein funktionierendes wissen über Netzwerk-und Netzwerk Verwaltungs Konzepte sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4e31-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a4e31-127">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="a4e31-127">Run-time requirements</span></span>

<span data-ttu-id="a4e31-128">Weitere Informationen zum Betriebssystem, das für die Verwendung einer bestimmten Funktion erforderlich ist, finden Sie im Abschnitt "Anforderungen" der Referenzseite für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="a4e31-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a4e31-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a4e31-129">In this section</span></span>



| <span data-ttu-id="a4e31-130">Thema</span><span class="sxs-lookup"><span data-stu-id="a4e31-130">Topic</span></span>                                                                                                | <span data-ttu-id="a4e31-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4e31-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4e31-132">Neues in SNMP</span><span class="sxs-lookup"><span data-stu-id="a4e31-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="a4e31-133">Informationen zu Updates von SNMP.</span><span class="sxs-lookup"><span data-stu-id="a4e31-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="a4e31-134">Simple Network Management-Protokoll (SNMP)</span><span class="sxs-lookup"><span data-stu-id="a4e31-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="a4e31-135">Informationen und API-Referenz für SNMP, einschließlich der SNMP-Verwaltungs-API, der SNMP-Erweiterungs-Agent-API und der API-Funktionen des SNMP-Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="a4e31-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="a4e31-136">WinSNMP-API</span><span class="sxs-lookup"><span data-stu-id="a4e31-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="a4e31-137">Informationen und API-Referenz für die Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (WinSNMP-API).</span><span class="sxs-lookup"><span data-stu-id="a4e31-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="a4e31-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4e31-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e31-139">Dynamic Host Configuration-Protokoll (DHCP)</span><span class="sxs-lookup"><span data-stu-id="a4e31-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="a4e31-140">Netzwerkverwaltung</span><span class="sxs-lookup"><span data-stu-id="a4e31-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="a4e31-141">Routing- und RAS-Dienst</span><span class="sxs-lookup"><span data-stu-id="a4e31-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

