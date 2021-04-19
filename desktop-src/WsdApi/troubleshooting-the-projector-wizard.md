---
description: Listet die Diagnose Prozeduren auf, die bei der Problembehandlung für den Projektor-Assistenten
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Problembehandlung beim Projektor-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360033"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="21c8f-103">Problembehandlung beim Projektor-Assistenten</span><span class="sxs-lookup"><span data-stu-id="21c8f-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="21c8f-104">Der Projektor-Assistent:</span><span class="sxs-lookup"><span data-stu-id="21c8f-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="21c8f-105">Verwendet für die Geräte Ermittlung immer UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="21c8f-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="21c8f-106">Verwendet immer http für Metadatenaustausch</span><span class="sxs-lookup"><span data-stu-id="21c8f-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="21c8f-107">Verwendet manchmal die gesteuerte Ermittlung</span><span class="sxs-lookup"><span data-stu-id="21c8f-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="21c8f-108">Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit dem Projektor-Assistenten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="21c8f-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="21c8f-109">**So beheben Sie Probleme mit dem Projektor-Assistenten**</span><span class="sxs-lookup"><span data-stu-id="21c8f-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="21c8f-110">Wenn die gesteuerte Ermittlung verwendet wird, beheben Sie die Fehler bei der [gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="21c8f-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="21c8f-111">Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="21c8f-112">[Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="21c8f-113">[Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="21c8f-114">[Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="21c8f-115">[Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="21c8f-116">[Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="21c8f-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="21c8f-117">[Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="21c8f-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="21c8f-118">Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="21c8f-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21c8f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21c8f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21c8f-120">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="21c8f-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



