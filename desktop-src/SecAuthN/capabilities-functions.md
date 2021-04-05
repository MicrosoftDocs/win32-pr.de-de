---
description: Die Netzwerkanbieter-API gibt eine Funktion mit einer einzelnen Funktion an.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funktionen-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042014"
---
# <a name="capabilities-functions"></a><span data-ttu-id="62b6b-103">Funktionen-Funktionen</span><span class="sxs-lookup"><span data-stu-id="62b6b-103">Capabilities Functions</span></span>

<span data-ttu-id="62b6b-104">Die Netzwerkanbieter-API gibt eine Funktion mit einer einzelnen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="62b6b-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="62b6b-105">Wenn das Betriebssysteminformationen zu den Funktionen eines Netzwerk Anbieters anfordert, ruft der [*multianbieterrouter*](/windows/desktop/SecGloss/m-gly) (MPR) die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion jedes Netzwerk Anbieters auf, dessen Netzwerk aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="62b6b-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="62b6b-106">Die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion gibt eine Bitmaske zurück, die angibt, welche Funktionen der Netzwerkanbieter-API der Netzwerkanbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62b6b-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="62b6b-107">Die **NPgetCaps** -Funktion ist die einzige Funktion, die ein Netzwerkanbieter implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="62b6b-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="62b6b-108">Das Betriebssystem ruft diese Funktion auf, um zu bestimmen, welche anderen Funktionen der Netzwerkanbieter-API der Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62b6b-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
