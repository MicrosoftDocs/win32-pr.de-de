---
description: Ein debugtoolset, das auf Web Services on Devices API (WSDAPI) basiert, ist im Windows SDK und im Windows-Treiberkit (WDK) verfügbar.
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Debugtools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131824"
---
# <a name="debugging-tools"></a><span data-ttu-id="5aa0c-103">Debugtools</span><span class="sxs-lookup"><span data-stu-id="5aa0c-103">Debugging Tools</span></span>

<span data-ttu-id="5aa0c-104">Ein debugtoolset, das auf Web Services on Devices API (WSDAPI) basiert, ist im Windows SDK und im Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-104">A debugging toolset built on Web Services on Devices API (WSDAPI) is available in the Windows SDK and the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="5aa0c-105">Mit diesen Tools können Sie die Funktionalität von benutzerdefinierten Anwendungen testen, die auf WSDAPI geschrieben wurden, oder Geräte und Clients, die mit einem anderen Geräte Profil für Webdienst Stapel (DPWS) geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-105">These tools can be used to test the functionality of custom applications written on WSDAPI, or devices and clients written using other Device Profile for Web Services (DPWS) stacks.</span></span>

<span data-ttu-id="5aa0c-106">Mithilfe der WSD-Debug-Hosts (wsddebug \_ -host.exe) und WSD Debug-Client (wsddebug \_client.exe)-Tools können Sie die Merkmale von DPWS-Clients oder-Hosts überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-106">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools can be used to inspect the characteristics of DPWS clients or hosts.</span></span> <span data-ttu-id="5aa0c-107">Sie können auch verwendet werden, um Konnektivitätsprobleme oder Konfigurationsprobleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-107">They can also be used to troubleshoot connectivity or configuration problems.</span></span> <span data-ttu-id="5aa0c-108">Weitere Informationen finden Sie im [Handbuch zur Problembehandlung für WSDAPI](wsdapi-troubleshooting-guide.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0c-108">For more information, see [WSDAPI Troubleshooting Guide](wsdapi-troubleshooting-guide.md).</span></span> <span data-ttu-id="5aa0c-109">Diese Tools sind nur im SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-109">These tools are only available in the SDK.</span></span> <span data-ttu-id="5aa0c-110">Die SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-110">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="5aa0c-111">Das [WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) kann verwendet werden, um die Interoperabilität auf SOAP-oder auf Transport Ebene zu testen (d. h. sicherzustellen, dass Nachrichten wohl geformt sind).</span><span class="sxs-lookup"><span data-stu-id="5aa0c-111">The [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) can be used to test SOAP-level or transport-level interoperability (that is, ensuring messages are well-formed).</span></span> <span data-ttu-id="5aa0c-112">Dieses Tool ist nur im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-112">This tool is only available in the WDK.</span></span>

## <a name="the-wsd-debug-client"></a><span data-ttu-id="5aa0c-113">Der WSD-Debugclient</span><span class="sxs-lookup"><span data-stu-id="5aa0c-113">The WSD Debug Client</span></span>

<span data-ttu-id="5aa0c-114">Der WSD-Debugclient (wsddebug- \_client.exe) bietet eine interaktive Konsole, die zum Senden und empfangen von WS-Discovery Meldungen und zum Abrufen von Metadaten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-114">The WSD Debug Client (wsddebug\_client.exe) provides an interactive console that can be used to send and receive WS-Discovery messages, and to obtain metadata.</span></span> <span data-ttu-id="5aa0c-115">Sie kann auch verwendet werden, um unformatierte Multicast Nachrichten zu generieren und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-115">It can also be used to generate and consume raw multicast messages.</span></span>

<span data-ttu-id="5aa0c-116">Der WSD-Debugclient kann in einem von drei Modi betrieben werden: Multicast, Ermittlung und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-116">The WSD Debug Client operates in one of three modes: multicast, discovery, and metadata.</span></span>



| <span data-ttu-id="5aa0c-117">Mode</span><span class="sxs-lookup"><span data-stu-id="5aa0c-117">Mode</span></span>      | <span data-ttu-id="5aa0c-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5aa0c-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa0c-119">Multicast</span><span class="sxs-lookup"><span data-stu-id="5aa0c-119">Multicast</span></span> | <span data-ttu-id="5aa0c-120">Im Multicast Modus sendet und empfängt der WSD-Debugclient nicht formatierte Multicast Nachrichten an UDP-Port 3702, wie in WS-Discovery definiert.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-120">In Multicast mode, the WSD Debug Client sends and receives unformatted multicast messages on UDP port 3702, as defined in WS-Discovery.</span></span> <span data-ttu-id="5aa0c-121">Der Benutzer kann diese SOAP-Nachrichten in einer Textdatei speichern und die Nachrichten mit dem WSD-Debugclient ändern und erneut übertragen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-121">The user may save these SOAP messages in a text file, and may modify and rebroadcast the messages with the WSD Debug Client.</span></span>                                                                                                                                 |
| <span data-ttu-id="5aa0c-122">Ermittlung</span><span class="sxs-lookup"><span data-stu-id="5aa0c-122">Discovery</span></span> | <span data-ttu-id="5aa0c-123">Im Ermittlungs Modus sendet und empfängt der WSD-Debugclient formatierte WS-Discovery Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-123">In Discovery mode, the WSD Debug Client sends and receives formatted WS-Discovery messages.</span></span> <span data-ttu-id="5aa0c-124">Sie kann empfangene Meldungen [Hello](hello-message.md), [Bye](bye-message.md), [Probe Matches](probematches-message.md)und [resolvematches](resolvematches-message.md) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-124">It can display received [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="5aa0c-125">Er kann Testnachrichten über UDP oder [http senden und Nachrichten über](probe-message.md) UDP [Auflösen](resolve-message.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa0c-125">It can send [Probe](probe-message.md) messages over UDP or HTTP, and [Resolve](resolve-message.md) messages over UDP.</span></span> |
| <span data-ttu-id="5aa0c-126">Metadaten</span><span class="sxs-lookup"><span data-stu-id="5aa0c-126">Metadata</span></span>  | <span data-ttu-id="5aa0c-127">Zusätzlich zur Implementierung aller Features des Ermittlungs Modus versucht der metadatenmodus auch, Metadaten von Geräten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-127">In addition to implementing all of the features of Discovery mode, Metadata mode also attempts to retrieve metadata from devices.</span></span>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="5aa0c-128">Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Verwenden eines generischen Hosts und Clients für die UDP-WS-](using-a-generic-host-and-client-for-udp-ws-discovery.md)Ermittlung und [Verwenden des WSD-Debugclients zum Überprüfen von Multicast Datenverkehr](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0c-128">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md), and [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

## <a name="the-wsd-debug-host"></a><span data-ttu-id="5aa0c-129">Der WSD-debughost</span><span class="sxs-lookup"><span data-stu-id="5aa0c-129">The WSD Debug Host</span></span>

<span data-ttu-id="5aa0c-130">Der WSD-debughost (wsddebug- \_host.exe) stellt eine interaktive Konsole bereit, mit der der Host angekündigt, auf Client Anforderungen reagiert und Diagnoseinformationen ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-130">The WSD Debug Host (wsddebug\_host.exe) provides an interactive console used to announce the host, respond to client requests, and print diagnostic information.</span></span>

<span data-ttu-id="5aa0c-131">Der WSD-debughost funktioniert in einem von zwei Modi: Ermittlung und Metadaten.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-131">The WSD Debug Host operates in one of two modes: discovery and metadata.</span></span>



| <span data-ttu-id="5aa0c-132">Mode</span><span class="sxs-lookup"><span data-stu-id="5aa0c-132">Mode</span></span>      | <span data-ttu-id="5aa0c-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5aa0c-133">Description</span></span>                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa0c-134">Ermittlung</span><span class="sxs-lookup"><span data-stu-id="5aa0c-134">Discovery</span></span> | <span data-ttu-id="5aa0c-135">Im Ermittlungs Modus druckt der WSD-debughost formatierte WS-Discovery Meldungen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-135">In Discovery mode, the WSD Debug Host prints formatted WS-Discovery messages.</span></span> <span data-ttu-id="5aa0c-136">Außerdem sendet Sie [Hello](hello-message.md) -und [Bye](bye-message.md) -Nachrichten und antwortet [automatisch auf Test](probe-message.md) -und [Auflösungs](resolve-message.md) Meldungen.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-136">It also sends [Hello](hello-message.md) and [Bye](bye-message.md) messages, and automatically responds to [Probe](probe-message.md) and [Resolve](resolve-message.md) messages.</span></span> |
| <span data-ttu-id="5aa0c-137">Metadaten</span><span class="sxs-lookup"><span data-stu-id="5aa0c-137">Metadata</span></span>  | <span data-ttu-id="5aa0c-138">Zusätzlich zur Implementierung aller Features des Ermittlungs Modus gibt der metadatenmodus einen Metadatendienst aus und ermöglicht Clients das Herstellen einer Verbindung und das Ausführen von Metadatenaustausch.</span><span class="sxs-lookup"><span data-stu-id="5aa0c-138">In addition to implementing all of the features of Discovery mode, Metadata mode advertises a metadata service and allows clients to connect and perform metadata exchange.</span></span>                                                                                       |



 

<span data-ttu-id="5aa0c-139">Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md) und [Verwenden eines generischen Hosts und Clients für UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0c-139">For more information, see [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa0c-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5aa0c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa0c-141">WSD-Anwendungsentwicklung unter Windows</span><span class="sxs-lookup"><span data-stu-id="5aa0c-141">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="5aa0c-142">WSDAPI-Entwicklungs Tools</span><span class="sxs-lookup"><span data-stu-id="5aa0c-142">WSDAPI Development Tools</span></span>](wsdapi-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5aa0c-143">WSDAPI-Handbuch zur Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="5aa0c-143">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



