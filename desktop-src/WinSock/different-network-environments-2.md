---
description: Mehrere Netzwerkumgebungen wirken sich auf das Netzwerk Verhalten einer Anwendung aus.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Unterschiedliche Netzwerkumgebungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218951"
---
# <a name="different-network-environments"></a><span data-ttu-id="ead47-103">Unterschiedliche Netzwerkumgebungen</span><span class="sxs-lookup"><span data-stu-id="ead47-103">Different Network Environments</span></span>

<span data-ttu-id="ead47-104">Mehrere Netzwerkumgebungen wirken sich auf das Netzwerk Verhalten einer Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="ead47-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="ead47-105">Zu den Eigenschaften, die Netzwerkumgebungen unterscheiden, gehören niedrige und hohe Bandbreite und niedrige und hohe RTT.</span><span class="sxs-lookup"><span data-stu-id="ead47-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="ead47-106">Netzwerkumgebungen wirken sich auf die Transaktions-und Streaminganwendungen auf unterschiedliche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="ead47-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="ead47-107">Transaktionale Anwendungen sind sensibler für RTT. Streaming-Anwendungen sind sensibler für Produkte mit Bandbreiten Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="ead47-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![Diagramm, das zeigt, wie sich unterschiedliche Netzwerkumgebungen auf das Netzwerk Verhalten einer Anwendung auswirken.](images/hperf-1.png)

<span data-ttu-id="ead47-109">Einwählnetzwerke und einige drahtlose Netzwerke haben eine Variable RTT.</span><span class="sxs-lookup"><span data-stu-id="ead47-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="ead47-110">Satelliten Netzwerke verfügen in der Regel über eine asymmetrische Bandbreite zwischen Upstream und Downstream.</span><span class="sxs-lookup"><span data-stu-id="ead47-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="ead47-111">Wireless LAN und xDSL sind gute Beispiele für Netzwerke mit Produkten für die Bandbreiten Verzögerung, die denen von Fast Ethernet ähneln.</span><span class="sxs-lookup"><span data-stu-id="ead47-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ead47-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ead47-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead47-113">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ead47-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ead47-114">Leistungsdimensionen</span><span class="sxs-lookup"><span data-stu-id="ead47-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



