---
description: Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Netzwerkanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217318"
---
# <a name="network-providers"></a><span data-ttu-id="4ce57-103">Netzwerkanbieter</span><span class="sxs-lookup"><span data-stu-id="4ce57-103">Network Providers</span></span>

<span data-ttu-id="4ce57-104">Ein Netzwerkanbieter ist eine DLL, die ein bestimmtes Netzwerkprotokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ce57-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="4ce57-105">Außerdem wird die [Netzwerkanbieter-API](network-provider-api.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="4ce57-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="4ce57-106">Dies ermöglicht es, mit dem Windows-Betriebssystem zu interagieren, um Standard Netzwerk Anforderungen zu erhalten, z. b. Verbindungs-oder Verbindungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="4ce57-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="4ce57-107">Um diese Anforderungen zu verarbeiten, ruft der Netzwerkanbieter die Netzwerk spezifische API auf, die für das Netzwerkprotokoll geeignet ist, das vom Netzwerkanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4ce57-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="4ce57-108">Anders ausgedrückt: der Netzwerkanbieter umschließt die Netzwerk spezifischen Funktionen in einer DLL, die eine Standardschnittstelle für Windows verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4ce57-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="4ce57-109">Mithilfe von Netzwerkanbietern kann Windows viele verschiedene Arten von Netzwerkprotokollen unterstützen, ohne die Netzwerk spezifischen Details der einzelnen Netzwerke kennen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4ce57-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="4ce57-110">Dies ist von entscheidender Bedeutung, da immer neue Netzwerkprotokolle entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="4ce57-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="4ce57-111">Mit Netzwerkanbietern ist für die Unterstützung eines neuen Protokolls lediglich das Erstellen und Installieren eines neuen Netzwerk Anbieters erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ce57-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="4ce57-112">Informationen zu den Funktionen und Strukturen von Netzwerkanbietern finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4ce57-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="4ce57-113">Netzwerkanbieter Funktionen</span><span class="sxs-lookup"><span data-stu-id="4ce57-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="4ce57-114">Netzwerkanbieter Strukturen</span><span class="sxs-lookup"><span data-stu-id="4ce57-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



