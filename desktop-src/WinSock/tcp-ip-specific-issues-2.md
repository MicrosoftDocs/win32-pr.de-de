---
description: Bestimmte Programmiertechniken stoßen auf Leistungsprobleme, die mit der Implementierung von TCP/IP verknüpft sind.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: TCP/IP-spezifische Probleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363522"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="efb94-103">TCP/IP-spezifische Probleme</span><span class="sxs-lookup"><span data-stu-id="efb94-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="efb94-104">Bestimmte Programmiertechniken stoßen auf Leistungsprobleme, die mit der Implementierung von TCP/IP verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="efb94-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="efb94-105">Diese Leistungsprobleme deuten nicht darauf hin, dass TCP/IP ineffizient ist oder einen Leistungsengpass verursacht. Diese Probleme werden vielmehr erkannt, wenn TCP/IP-Vorgänge nicht verstanden werden.</span><span class="sxs-lookup"><span data-stu-id="efb94-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="efb94-106">Die folgenden Probleme identifizieren häufige Szenarien, in denen die Kombination von TCP/IP-Betriebs-und Netzwerk Anwendungs Entwicklungsoptionen zu schlechter Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="efb94-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="efb94-107">Verbinden Sie große Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="efb94-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="efb94-108">Einige Anwendungen instanziieren eine neue TCP-Verbindung für jede Transaktion.</span><span class="sxs-lookup"><span data-stu-id="efb94-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="efb94-109">Das Einrichten der TCP-Verbindung nimmt Zeit in Betrieb, leistet zusätzliche RTTS und unterliegt einem langsamen Start.</span><span class="sxs-lookup"><span data-stu-id="efb94-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="efb94-110">Außerdem unterliegen die geschlossenen Verbindungen der Wartezeit, die Systemressourcen beansprucht.</span><span class="sxs-lookup"><span data-stu-id="efb94-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="efb94-111">Verbindungs intensive Anwendungen sind größtenteils üblich, weil Sie einfach zu erstellen sind. die Test-und Fehlerbehandlung ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="efb94-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="efb94-112">Das Erkennen von Fehlern bei einer permanenten Verbindung kann viel Code und Aufwand in Anspruch nehmen und ist daher manchmal nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="efb94-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="efb94-113">Beheben Sie diese Situation, indem Sie die TCP-Verbindung wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="efb94-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="efb94-114">Dies kann die Serialisierung über die TCP-Verbindung bewirken, es sei denn, die Transaktionen werden über mehrere Verbindungen multiplext.</span><span class="sxs-lookup"><span data-stu-id="efb94-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="efb94-115">Wenn dieser Ansatz verwendet wird, sollte die Anzahl der Verbindungen auf zwei begrenzt werden, und es sind die Rahmen-und erweiterte Fehlerbehandlung auf Anwendungsebene erforderlich.</span><span class="sxs-lookup"><span data-stu-id="efb94-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="efb94-116">Sendepuffer der Länge 0 (null) und blockierende Sende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="efb94-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="efb94-117">Das Deaktivieren der Pufferung mithilfe der Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) zum Festlegen des Sendepuffers ( \_ sndbuf) auf 0 (null) ähnelt dem Ausschalten der Datenträger Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="efb94-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="efb94-118">Wenn der Sendepuffer auf NULL festgelegt und blockierende Sende Vorgänge ausgegeben werden, hat eine Anwendung eine Wahrscheinlichkeit von 50 Prozent, dass eine verzögerte Bestätigung von 200 Millisekunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="efb94-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="efb94-119">Deaktivieren Sie Send buffereing nicht, es sei denn, Sie haben die Auswirkungen in allen Netzwerkumgebungen in Betracht gezogen.</span><span class="sxs-lookup"><span data-stu-id="efb94-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="efb94-120">Eine Ausnahme: beim Streamen von Daten mithilfe von überlappenden e/a-Vorgängen sollte der Sendepuffer auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="efb94-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="efb94-121">Send-Send-Receive-Programmiermodell.</span><span class="sxs-lookup"><span data-stu-id="efb94-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="efb94-122">Die Strukturierung einer Anwendung für die Durchführung von Send-Send-Receive erhöht die Wahrscheinlichkeit, dass Sie den Nagle-Algorithmus findet, was eine Verzögerung von RTT + 200 MS verursacht.</span><span class="sxs-lookup"><span data-stu-id="efb94-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="efb94-123">Der Nagle-Algorithmus kann auftreten, wenn der letzte Sendevorgang kleiner ist als die maximale TCP-Segment Größe (MSS, die maximale Datenmenge in einem einzelnen Datagramm).</span><span class="sxs-lookup"><span data-stu-id="efb94-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="efb94-124">MSS kann ein sehr großer Wert (64K in IPv4 und noch größer in IPv6) sein. Achten Sie daher nicht auf einen normalerweise kleinen MSS.</span><span class="sxs-lookup"><span data-stu-id="efb94-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="efb94-125">Eine bessere Option besteht darin, die beiden Sendungen mithilfe der [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -oder **memcpy** -Funktion in einem einzelnen Sendevorgang zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="efb94-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="efb94-126">Eine große Anzahl gleichzeitiger Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="efb94-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="efb94-127">Gleichzeitige Verbindungen sollten höchstens zwei überschreiten, außer in speziellen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="efb94-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="efb94-128">Wenn zwei gleichzeitige Verbindungen überschritten werden, werden Ressourcen verschwendet.</span><span class="sxs-lookup"><span data-stu-id="efb94-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="efb94-129">Eine gute Regel besteht darin, bis zu vier kurzlebige Verbindungen oder zwei persistente Verbindungen pro Ziel zu haben.</span><span class="sxs-lookup"><span data-stu-id="efb94-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efb94-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efb94-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb94-131">Anwendungsverhalten</span><span class="sxs-lookup"><span data-stu-id="efb94-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="efb94-132">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="efb94-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="efb94-133">Nagle-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="efb94-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



