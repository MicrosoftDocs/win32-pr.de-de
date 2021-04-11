---
description: Netzwerkmonitor ist eine Komponente von Microsoft Systems Management Server (SMS), die zum erkennen und Beheben von Problemen auf LANs, Wens und seriellen Links verwendet wird, auf denen Microsoft Remote Access Server (RAS) ausgeführt wird.
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Informationen zu Netzwerkmonitor 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042228"
---
# <a name="about-network-monitor-21"></a><span data-ttu-id="ce9c9-103">Informationen zu Netzwerkmonitor 2,1</span><span class="sxs-lookup"><span data-stu-id="ce9c9-103">About Network Monitor 2.1</span></span>

<span data-ttu-id="ce9c9-104">Netzwerkmonitor ist eine Komponente von Microsoft Systems Management Server (SMS), die zum erkennen und Beheben von Problemen auf LANs, Wens und seriellen Links verwendet wird, auf denen Microsoft Remote Access Server (RAS) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-104">Network Monitor is a component of Microsoft Systems Management Server (SMS) used to detect and troubleshoot problems on LANs, WANs, and serial links running Microsoft Remote Access Server (RAS).</span></span> <span data-ttu-id="ce9c9-105">Netzwerkmonitor stellt die Analyse von Netzwerkdaten nach der Erfassung bereit.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-105">Network Monitor provides post-capture network data analysis.</span></span>

<span data-ttu-id="ce9c9-106">Bei der Analyse nach der Erfassung wird der Netzwerk Datenverkehr in einer proprietären Erfassungs Datei gespeichert, sodass die erfassten Daten später analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-106">In post-capture analysis, network traffic is saved in a proprietary capture file, so that the captured data can be analyzed later.</span></span> <span data-ttu-id="ce9c9-107">In diesem Fall kann die Analyse in Form von Protokoll- [*Parser*](p.md) vorliegen, die bestimmte Netzwerk Frame Typen auswählen und die Frame Daten in der Netzwerkmonitor-Benutzeroberfläche anzeigen. oder die Analyse kann in Form von [*Experten*](e.md) vorliegen, die die Netzwerkdaten untersuchen und einen Bericht anzeigen (Experten können auch die Netzwerkdaten verändern).</span><span class="sxs-lookup"><span data-stu-id="ce9c9-107">In this case, analysis can be in the form of protocol [*parsers*](p.md) picking out specific network frame types and displaying the frame data in the Network Monitor UI; or analysis can be in the form of [*experts*](e.md) examining the network data and displaying a report (experts may also manipulate the network data).</span></span>

<span data-ttu-id="ce9c9-108">Netzwerkmonitor stellt die folgenden Arten von Funktionen bereit:</span><span class="sxs-lookup"><span data-stu-id="ce9c9-108">Network Monitor provides the following types of functionality:</span></span>

-   <span data-ttu-id="ce9c9-109">Erfasst Netzwerkdaten im Echtzeitmodus oder im verzögerten Modus.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-109">Captures network data in real-time or delayed mode.</span></span>
-   <span data-ttu-id="ce9c9-110">Stellt Filterfunktionen beim Erfassen von Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-110">Provides filtering capabilities when capturing data.</span></span>
-   <span data-ttu-id="ce9c9-111">Verwendet Experten und Parser für eine ausführliche nach Erfassungs Analyse.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-111">Uses experts and parsers for detailed post-capture analysis.</span></span>

<span data-ttu-id="ce9c9-112">Weitere Informationen zu Netzwerkmonitor Funktionen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ce9c9-112">For more information about Network Monitor features, see:</span></span>

-   [<span data-ttu-id="ce9c9-113">Architektur von Experten und Parsers</span><span class="sxs-lookup"><span data-stu-id="ce9c9-113">Expert and Parser Architecture</span></span>](expert-and-parser-architecture.md)
-   [<span data-ttu-id="ce9c9-114">Experten</span><span class="sxs-lookup"><span data-stu-id="ce9c9-114">Experts</span></span>](experts.md)
-   [<span data-ttu-id="ce9c9-115">Parser</span><span class="sxs-lookup"><span data-stu-id="ce9c9-115">Parsers</span></span>](parsers.md)
-   [<span data-ttu-id="ce9c9-116">Netzwerk Paketanbieter</span><span class="sxs-lookup"><span data-stu-id="ce9c9-116">Network Packet Providers</span></span>](network-packet-providers.md)
-   [<span data-ttu-id="ce9c9-117">BlobNetzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="ce9c9-117">Network Monitor BLOBs</span></span>](network-monitor-blobs.md)
-   [<span data-ttu-id="ce9c9-118">Seite "Ereignis Verweis"</span><span class="sxs-lookup"><span data-stu-id="ce9c9-118">Event Reference Page</span></span>](event-reference-page.md)
-   [<span data-ttu-id="ce9c9-119">Erfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="ce9c9-119">Capture Filters</span></span>](capture-filters.md)

<span data-ttu-id="ce9c9-120">**Windows Vista:** Netzwerkmonitor 2,1 und frühere Versionen werden auf dieser Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce9c9-120">**Windows Vista:** Network Monitor 2.1 and earlier are not supported on this platform.</span></span>

 

 



