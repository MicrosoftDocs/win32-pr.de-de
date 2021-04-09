---
description: PCs mit Microsoft Windows verfügen häufig über zahlreiche Netzwerkverbindungen, z. b. mehrere Netzwerkschnittstellenkarten (NIC), die mit unterschiedlichen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Network Location Awareness Service Provider (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129144"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="97755-103">Network Location Awareness Service Provider (NLA)</span><span class="sxs-lookup"><span data-stu-id="97755-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="97755-104">PCs mit Microsoft Windows verfügen häufig über zahlreiche Netzwerkverbindungen, z. b. mehrere Netzwerkschnittstellenkarten (NIC), die mit unterschiedlichen Netzwerken verbunden sind, oder eine physische Netzwerkverbindung und eine DFÜ-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="97755-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="97755-105">Windows Sockets ist in der Lage, verfügbare Netzwerkschnittstellen für einige Zeit aufzulisten, aber bestimmte wichtige Informationen zu Netzwerkverbindungen waren zuvor nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97755-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="97755-106">Hierzu gehören Informationen wie z. b. das logische Netzwerk, an das ein Windows-Computer angefügt ist, oder ob mehrere Schnittstellen mit dem gleichen Netzwerk verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="97755-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="97755-107">Der Network Location Awareness Service-Anbieter, der üblicherweise als NLA bezeichnet wird, ermöglicht Windows Sockets 2-Anwendungen, das logische Netzwerk zu identifizieren, an das ein Windows-Computer angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="97755-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="97755-108">Außerdem ermöglicht NLA Windows Sockets-Anwendungen zu identifizieren, an welche physische Netzwerkschnittstelle eine bestimmte Anwendung bestimmte Informationen gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="97755-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="97755-109">NLA wird als generischer Dienstanbieter für Windows Sockets 2-Namensauflösung implementiert.</span><span class="sxs-lookup"><span data-stu-id="97755-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



