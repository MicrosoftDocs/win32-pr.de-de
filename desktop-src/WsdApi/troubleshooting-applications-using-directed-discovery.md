---
description: Anwendungen, die die gesteuerte Ermittlung verwenden, senden Testnachrichten über HTTP oder HTTPS, um Geräte zu ermitteln.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Problembehandlung bei WSDAPI-Anwendungen mithilfe der gesteuerten Ermittlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528574"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="874d3-103">Problembehandlung bei WSDAPI-Anwendungen mithilfe der gesteuerten Ermittlung</span><span class="sxs-lookup"><span data-stu-id="874d3-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="874d3-104">Anwendungen, die die gesteuerte Ermittlung verwenden [, senden Test](probe-message.md) Nachrichten über HTTP oder HTTPS, um Geräte zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="874d3-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="874d3-105">Die entsprechenden [Probe Matches](probematches-message.md) -Nachrichten, die als Antwort gesendet werden, werden auch über HTTP oder HTTPS gesendet.</span><span class="sxs-lookup"><span data-stu-id="874d3-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="874d3-106">Die gesteuerte Ermittlung kann mit dem Assistenten zum Hinzufügen von Druckern, einem Funktions Ermittlungs Client oder einer WSDAPI-Anwendung initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="874d3-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="874d3-107">Die Test-und Probe Matches-Meldungen sind strukturell identisch mit den über UDP gesendeten.</span><span class="sxs-lookup"><span data-stu-id="874d3-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="874d3-108">Den Nachrichten werden die entsprechenden http-oder HTTPS-Header vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="874d3-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="874d3-109">Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung mithilfe der gesteuerten Ermittlung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="874d3-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="874d3-110">**So beheben Sie Probleme mit einer WSDAPI-Anwendung mithilfe der gesteuerten Ermittlung**</span><span class="sxs-lookup"><span data-stu-id="874d3-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="874d3-111">Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="874d3-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="874d3-112">[Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="874d3-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="874d3-113">[Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="874d3-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="874d3-114">[Überprüfen Sie die Netzwerk Ablauf Verfolgungen für eine Anwendung mithilfe der gesteuerten](inspecting-network-traces-for-applications-using-directed-discovery.md)Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="874d3-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="874d3-115">Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="874d3-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="874d3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="874d3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="874d3-117">Ersten Schritte mit der WSDAPI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="874d3-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="874d3-118">Problembehandlung beim Hinzufügen von Drucker</span><span class="sxs-lookup"><span data-stu-id="874d3-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="874d3-119">Problembehandlung bei WSDAPI-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="874d3-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



