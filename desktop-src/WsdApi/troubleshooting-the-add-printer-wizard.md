---
description: Listet die Diagnose Prozeduren auf, die bei der Problembehandlung des druckerdruckerassistenten
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Problembehandlung beim Hinzufügen von Drucker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357484"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="8040f-103">Problembehandlung beim Hinzufügen von Drucker</span><span class="sxs-lookup"><span data-stu-id="8040f-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="8040f-104">Der Assistent zum Hinzufügen von Druckern:</span><span class="sxs-lookup"><span data-stu-id="8040f-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="8040f-105">Verwendet für die Geräte Ermittlung immer UDP-WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="8040f-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="8040f-106">Initiiert immer eine HTTP-oder HTTPS-Verbindung für den Metadatenaustausch.</span><span class="sxs-lookup"><span data-stu-id="8040f-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="8040f-107">Verwendet manchmal die gesteuerte Ermittlung</span><span class="sxs-lookup"><span data-stu-id="8040f-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="8040f-108">Verwendet manchmal einen sicheren Kanal (HTTPS) für den Metadatenaustausch</span><span class="sxs-lookup"><span data-stu-id="8040f-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="8040f-109">Die folgenden Diagnose Prozeduren sollten (in der Reihenfolge) verwendet werden, um Probleme mit dem Assistenten zum Hinzufügen von Druckern zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8040f-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="8040f-110">**So beheben Sie Probleme mit dem Assistenten zum Hinzufügen von Druckern**</span><span class="sxs-lookup"><span data-stu-id="8040f-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="8040f-111">Wenn die gesteuerte Ermittlung verwendet wird, beheben Sie die Fehler bei der [gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="8040f-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="8040f-112">Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="8040f-113">[Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="8040f-114">[Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="8040f-115">[Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="8040f-116">[Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="8040f-117">[Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="8040f-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="8040f-118">[Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="8040f-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="8040f-119">Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="8040f-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8040f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8040f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8040f-121">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="8040f-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="8040f-122">Problembehandlung bei Anwendungen mithilfe der gesteuerten Ermittlung</span><span class="sxs-lookup"><span data-stu-id="8040f-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



