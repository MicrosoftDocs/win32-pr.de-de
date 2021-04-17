---
description: Geräte Profile für Web Services (DPWS)-Hosts und-Clients kommunizieren über das Netzwerk, indem eine Reihe von SOAP-Nachrichten über UDP und HTTP verwendet wird.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Ermittlungs-und Metadatenaustausch-Nachrichten Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218952"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="a3d10-103">Ermittlungs-und Metadatenaustausch-Nachrichten Muster</span><span class="sxs-lookup"><span data-stu-id="a3d10-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="a3d10-104">Geräte Profile für Web Services (DPWS)-Hosts und-Clients kommunizieren über das Netzwerk, indem eine Reihe von SOAP-Nachrichten über UDP und HTTP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3d10-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="a3d10-105">Das folgende Diagramm zeigt eine Übersicht über den erwarteten UDP-und HTTP-Datenverkehr zwischen einem DPWS-Host und-Client.</span><span class="sxs-lookup"><span data-stu-id="a3d10-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Das Diagramm zeigt UDP-und HTTP-Datenverkehr zwischen einem DPWS-Host und-Client.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="a3d10-107">[Hello](hello-message.md)- [](bye-message.md), bye [-, Test-,](probe-message.md) [Resolve](resolve-message.md)-und [Get](get--metadata-exchange--http-request-and-message.md) -Nachrichten werden ohne Netzwerkanfrage generiert. Diese Nachrichten werden verwendet, um den Gerätestatus anzukündigen oder eine Such Anforderung auszugeben.</span><span class="sxs-lookup"><span data-stu-id="a3d10-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="a3d10-108">[Probe Matches](probematches-message.md), [resolvematches](resolvematches-message.md)und [GetResponse](getresponse--metadata-exchange--message.md) -Nachrichten werden als Antwort auf die Nachrichten "Probe", "auflösen" und "Get" generiert.</span><span class="sxs-lookup"><span data-stu-id="a3d10-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="a3d10-109">Die Nachrichten [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)und [resolvematches](resolvematches-message.md) werden immer über UDP ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3d10-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="a3d10-110">Ebenso erfolgen [Get](get--metadata-exchange--http-request-and-message.md) -und [GetResponse](getresponse--metadata-exchange--message.md) -metadatennachrichten immer über HTTP oder HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a3d10-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="a3d10-111">Test [-und](probe-message.md) [Probe Matches](probematches-message.md) -Nachrichten werden normalerweise über UDP übermittelt, aber über eine HTTP-oder HTTPS-Verbindung in einem gesteuerten Ermittlungs Szenario.</span><span class="sxs-lookup"><span data-stu-id="a3d10-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="a3d10-112">Weitere Informationen zu gerichteten Ermittlungs Nachrichten Mustern finden Sie unter [Problembehandlung bei Anwendungen mithilfe der gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="a3d10-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="a3d10-113">In der folgenden Liste wird die typische Nachrichten Sequenz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3d10-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="a3d10-114">Nicht alle Nachrichten sind obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="a3d10-114">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="a3d10-115">[Hello](hello-message.md) (Hallo)</span><span class="sxs-lookup"><span data-stu-id="a3d10-115">[Hello](hello-message.md)</span></span>
2.  [<span data-ttu-id="a3d10-116">Test</span><span class="sxs-lookup"><span data-stu-id="a3d10-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="a3d10-117">Probe Matches</span><span class="sxs-lookup"><span data-stu-id="a3d10-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="a3d10-118">Beheben</span><span class="sxs-lookup"><span data-stu-id="a3d10-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="a3d10-119">Resolvematches</span><span class="sxs-lookup"><span data-stu-id="a3d10-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="a3d10-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadatenaustauschanforderung)</span><span class="sxs-lookup"><span data-stu-id="a3d10-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="a3d10-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="a3d10-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="a3d10-122">Auf Wiedersehen</span><span class="sxs-lookup"><span data-stu-id="a3d10-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="a3d10-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3d10-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3d10-124">Informationen zu Webdiensten auf Geräten</span><span class="sxs-lookup"><span data-stu-id="a3d10-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



