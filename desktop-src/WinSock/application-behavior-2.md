---
description: Ein weiterer Aspekt der zu berücksichtigenden Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen Computern oder betriebsinternen Vorgängen sowie das Verhalten, wenn Vorgänge zwischen zwei vernetzten Computern stattfinden.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Anwendungsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526213"
---
# <a name="application-behavior"></a><span data-ttu-id="22c95-103">Anwendungsverhalten</span><span class="sxs-lookup"><span data-stu-id="22c95-103">Application Behavior</span></span>

<span data-ttu-id="22c95-104">Ein weiterer Aspekt der zu berücksichtigenden Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen Computern oder betriebsinternen Vorgängen sowie das Verhalten, wenn Vorgänge zwischen zwei vernetzten Computern stattfinden.</span><span class="sxs-lookup"><span data-stu-id="22c95-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="22c95-105">Es gibt Anwendungs Verhaltensweisen, die auf einem lokalen Computer möglicherweise akzeptabel sind, aber wenn Sie in einem Netzwerk ausgeführt werden, führen Sie zu erheblichen Leistungseinbußen und Ressourcenverbrauch.</span><span class="sxs-lookup"><span data-stu-id="22c95-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="22c95-106">Die folgenden Anwendungs Verhaltensweisen sollten bei der Entwicklung von Windows Sockets-Anwendungen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="22c95-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="22c95-107">Zu vermeide Verhalten</span><span class="sxs-lookup"><span data-stu-id="22c95-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="22c95-108">Chatty-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="22c95-108">Chatty Applications.</span></span>

    <span data-ttu-id="22c95-109">Einige Anwendungen führen viele kleine Transaktionen aus.</span><span class="sxs-lookup"><span data-stu-id="22c95-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="22c95-110">In Kombination mit dem Netzwerk Aufwand, der den einzelnen Transaktionen zugeordnet ist, wird der Effekt multipliziert.</span><span class="sxs-lookup"><span data-stu-id="22c95-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="22c95-111">In Netzwerken können kleine Transaktionen so viele Ressourcen und so viel Zeit wie große Transaktionen verbrauchen.</span><span class="sxs-lookup"><span data-stu-id="22c95-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="22c95-112">Ein besserer Ansatz ist die Kombination vieler kleiner Transaktionen zu einer einzelnen großen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="22c95-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="22c95-113">Serialisierte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="22c95-113">Serialized Transactions.</span></span>

    <span data-ttu-id="22c95-114">Unnötige Serialisierung von Transaktionen kann zu schlechter Leistung führen und die Skalierbarkeit beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="22c95-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="22c95-115">Beispielsweise nehmen 1000 serialisierte Transaktionen mindestens 1000 \* RTT zum Abschluss.</span><span class="sxs-lookup"><span data-stu-id="22c95-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="22c95-116">Ein besserer Ansatz besteht darin, nicht verbundene Transaktionen parallel auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22c95-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="22c95-117">Bei der Kombination von serialisierten Anwendungen mit ' geschwätzige '-Anwendungen kann die Reaktionsfähigkeit erheblich beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="22c95-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="22c95-118">Eine ordnungsgemäße Deserialisierung einer Anwendung kann schwierig sein.</span><span class="sxs-lookup"><span data-stu-id="22c95-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="22c95-119">Wenn die Änderung von serialisiert in parallel zu schwierig ist, sollten Sie mehrere Transaktionen in weniger großen Transaktionen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="22c95-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="22c95-120">FAT-Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="22c95-120">Fat Transactions.</span></span>

    <span data-ttu-id="22c95-121">Anwendungen, die unnötige Bytes im Netzwerk senden, werden als FAT-Anwendungen angesehen.</span><span class="sxs-lookup"><span data-stu-id="22c95-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="22c95-122">Anwendungen, die unnötige Bytes im Netzwerk senden, erhöhen den Netzwerk Mehraufwand, und die Leistung wird beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="22c95-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="22c95-123">Diese Situation tritt häufig von ineffizienten Datenstrukturen oder ineffizienten Datenstreaming auf.</span><span class="sxs-lookup"><span data-stu-id="22c95-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="22c95-124">Um dieses Problem zu beheben, optimieren Sie die Datenstrukturen, oder verwenden Sie die Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="22c95-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="22c95-125">In den folgenden Abschnitten werden Aspekte der zu berücksichtigenden Anwendungsentwicklung behandelt.</span><span class="sxs-lookup"><span data-stu-id="22c95-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="22c95-126">TCP/IP-spezifische Probleme</span><span class="sxs-lookup"><span data-stu-id="22c95-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="22c95-127">Erkennen langsamer Anwendungen</span><span class="sxs-lookup"><span data-stu-id="22c95-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="22c95-128">Berechnen des Aufwands mit netstat</span><span class="sxs-lookup"><span data-stu-id="22c95-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="22c95-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22c95-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c95-130">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="22c95-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



