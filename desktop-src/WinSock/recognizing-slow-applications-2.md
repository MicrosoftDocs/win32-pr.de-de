---
description: Dieser Leitfaden identifiziert eine langsame Anwendung als Microsoft Windows-Anwendung mit eingeschränkter Leistung.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Erkennen langsamer Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369776"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="114c4-103">Erkennen langsamer Anwendungen</span><span class="sxs-lookup"><span data-stu-id="114c4-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="114c4-104">Dieser Leitfaden identifiziert eine *langsame* Anwendung als Microsoft Windows-Anwendung mit eingeschränkter Leistung.</span><span class="sxs-lookup"><span data-stu-id="114c4-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="114c4-105">Eine langsame Anwendung weist eines oder mehrere der folgenden Symptome auf:</span><span class="sxs-lookup"><span data-stu-id="114c4-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="114c4-106">Die CPU-und Netzwerk Auslastung ist niedrig.</span><span class="sxs-lookup"><span data-stu-id="114c4-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="114c4-107">Der Computer scheint auf etwas zu warten.</span><span class="sxs-lookup"><span data-stu-id="114c4-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="114c4-108">Häufig wartet die Anwendung auf das Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="114c4-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="114c4-109">Wenn Sie den Nagle-Algorithmus mithilfe der TCP \_ nodelay-Socketoption ausschalten, wird die Leistung gesteigert.</span><span class="sxs-lookup"><span data-stu-id="114c4-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="114c4-110">Dies deutet auf andere Probleme hin und sollte nicht als Lösung betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="114c4-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="114c4-111">Wenn Sie den Nagle-Algorithmus ausschalten, erhöht sich der Protokoll Mehraufwand.</span><span class="sxs-lookup"><span data-stu-id="114c4-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="114c4-112">Verwenden Sie diese Methode nicht als Korrektur für die unterbrochenen Anwendungen – sondern nur als Anzeichen dafür, dass die Anwendung andere Aufgaben benötigt, um Leistungsprobleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="114c4-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="114c4-113">Die Anwendung stellt einen hohen mehr Aufwand dar.</span><span class="sxs-lookup"><span data-stu-id="114c4-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="114c4-114">Um den Anwendungs Aufwand zu berechnen, legen Sie fest, wie viele Daten in den einzelnen Richtungen übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="114c4-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="114c4-115">Verwenden Sie dann netstat, und fügen Sie (für Ethernet) 60 Bytes für jedes Paket und 500 Bytes für jede Verbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="114c4-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="114c4-116">Der beste Aufwand, der für das Streaming über Ethernet zu erwarten ist, beträgt ungefähr 6%.</span><span class="sxs-lookup"><span data-stu-id="114c4-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="114c4-117">Bei einer Modemverbindung liegt der beste Aufwand bei ungefähr 2%, da für einen PPP-Link die Header Komprimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114c4-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="114c4-118">Weitere Informationen finden Sie [unter Berechnen von Overhead mit netstat](calculating-overhead-with-netstat-2.md) .</span><span class="sxs-lookup"><span data-stu-id="114c4-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="114c4-119">Die Anwendungs Antwort wird verlangsamt, wenn die Verbindung über eine große RTT-Verbindung verfügt.</span><span class="sxs-lookup"><span data-stu-id="114c4-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="114c4-120">Wenn die Anwendung die Bandbreite des Links nicht nähert, sollte eine große RTT nur wenig oder gar keine Auswirkung haben.</span><span class="sxs-lookup"><span data-stu-id="114c4-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="114c4-121">Eine drastische Verlangsamung mit einem großen RTT ist ein deutliches Vorzeichen der serialisierten Verarbeitung und vieler kleiner Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="114c4-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="114c4-122">Jede Anwendung sollte in einer Umgebung mit einem großen RTT getestet werden.</span><span class="sxs-lookup"><span data-stu-id="114c4-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="114c4-123">Auf diese Weise werden die meisten Anwendungen angezeigt, die von schlechten Entwicklungsoptionen leiden.</span><span class="sxs-lookup"><span data-stu-id="114c4-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="114c4-124">Diese Tests können in verschiedenen Umgebungen durchgeführt werden, einschließlich eines drahtlosen LAN-Netzwerks, eines Verbindungs Verzögerungs Simulators oder eines Satelliten Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="114c4-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="114c4-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="114c4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="114c4-126">Anwendungsverhalten</span><span class="sxs-lookup"><span data-stu-id="114c4-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="114c4-127">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="114c4-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="114c4-128">Nagle-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="114c4-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



