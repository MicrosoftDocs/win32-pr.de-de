---
description: Berechnen des Aufwands mit netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Berechnen des Aufwands mit netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348182"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="926af-103">Berechnen des Aufwands mit netstat</span><span class="sxs-lookup"><span data-stu-id="926af-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="926af-104">Die Berechnung des Aufwands mit netstat sollte in einem stillen Netzwerk durchgeführt werden, um zu vermeiden, dass andere Netzwerk Datenverkehr von Daten verzerrt wird, z. b. Broadcast-oder Multicast Verkehr.</span><span class="sxs-lookup"><span data-stu-id="926af-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="926af-105">**So berechnen Sie den Netzwerk Aufwand einer Anwendung mithilfe von netstat**</span><span class="sxs-lookup"><span data-stu-id="926af-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="926af-106">Rufen Sie die aktuelle Schnittstellen Statistik mithilfe von netstat ab.</span><span class="sxs-lookup"><span data-stu-id="926af-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="926af-107">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="926af-107">Execute the application.</span></span>
3.  <span data-ttu-id="926af-108">Stellen Sie die Schnittstellen Statistik mit netstat wieder her.</span><span class="sxs-lookup"><span data-stu-id="926af-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="926af-109">Berechnen Sie die Anzahl der Bytes, die zwischen den beiden netstat-Messungen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="926af-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="926af-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="926af-110">Example</span></span>

<span data-ttu-id="926af-111">Das folgende Beispiel veranschaulicht diese Schritte, wobei Ttcp zum Senden von 10 Bytes an Daten, jeweils ein Byte, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="926af-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="926af-112">Zuerst wird ein theoretischer mehr Aufwand für die Anwendung berechnet.</span><span class="sxs-lookup"><span data-stu-id="926af-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="926af-113">Für diesen Test sind alle Pakete 60 bytes (das mindestens Ethernet).</span><span class="sxs-lookup"><span data-stu-id="926af-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="926af-114">Diese Übertragung erfordert drei Pakete, um die Verbindung einzurichten, 10 Datenpakete, 10 Bestätigungs Pakete (verzögerte Bestätigung wird fast jedes Mal ausgelöst) und vier Pakete, um die Verbindung ordnungsgemäß zu schließen.</span><span class="sxs-lookup"><span data-stu-id="926af-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="926af-115">Dies entspricht 27 Paketen mit jeweils 60 bytes, oder 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="926af-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="926af-116">Da nur 10 Bytes an Daten übertragen werden, beträgt der mehr Aufwand 1610 bytes, was über 99% Protokoll Mehraufwand liegt.</span><span class="sxs-lookup"><span data-stu-id="926af-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="926af-117">Befehle</span><span class="sxs-lookup"><span data-stu-id="926af-117">Commands</span></span>

<span data-ttu-id="926af-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="926af-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="926af-119">**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="926af-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="926af-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="926af-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="926af-121">Berechnungen</span><span class="sxs-lookup"><span data-stu-id="926af-121">Calculations</span></span>

<span data-ttu-id="926af-122">**Gesendet:** 816 bytes</span><span class="sxs-lookup"><span data-stu-id="926af-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="926af-123">**Empfangen:** 674 bytes</span><span class="sxs-lookup"><span data-stu-id="926af-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="926af-124">**Bytes gesamt:** 1490</span><span class="sxs-lookup"><span data-stu-id="926af-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="926af-125">**Benutzer bytes:** 10</span><span class="sxs-lookup"><span data-stu-id="926af-125">**User bytes:** 10</span></span>

<span data-ttu-id="926af-126">**Overhead:** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="926af-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="926af-127">\* \* Goodput: \* \* = 5 Bytes/Sekunde (oder 40 Bits/s)</span><span class="sxs-lookup"><span data-stu-id="926af-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="926af-128">Tatsächlich übertragene Bytes stimmen nicht mit den theoretischen Werten aus, da die Füll Zeichen nicht in den netstat-Werten berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="926af-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="926af-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="926af-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="926af-130">Anwendungsverhalten</span><span class="sxs-lookup"><span data-stu-id="926af-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="926af-131">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="926af-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



