---
title: Destinations
description: Ein Ziel in der Routing Tabelle ist ein Netzwerk Eintrag, der durch eine Netzwerkadresse und eine Netzwerk Maske repräsentiert wird.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856279"
---
# <a name="destinations"></a><span data-ttu-id="bef79-103">Destinations</span><span class="sxs-lookup"><span data-stu-id="bef79-103">Destinations</span></span>

<span data-ttu-id="bef79-104">Ein Ziel in der Routing Tabelle ist ein Netzwerk Eintrag, der durch eine Netzwerkadresse und eine Netzwerk Maske repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="bef79-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="bef79-105">Ein Ziel Eintrag in der Routing Tabelle umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bef79-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="bef79-106">Die Adresse, ausgedrückt als Netzwerkadresse und Netzwerk Maske.</span><span class="sxs-lookup"><span data-stu-id="bef79-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="bef79-107">Eine Liste der Routen zum Ziel.</span><span class="sxs-lookup"><span data-stu-id="bef79-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="bef79-108">Eine Liste der nicht transparenten Zeiger Slots.</span><span class="sxs-lookup"><span data-stu-id="bef79-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="bef79-109">Die Sichten, in denen dieses Ziel gültig ist.</span><span class="sxs-lookup"><span data-stu-id="bef79-109">The views in which this destination is valid.</span></span> <span data-ttu-id="bef79-110">Das Ziel enthält eine Struktur für jede Ansicht, die die folgenden Informationen enthält:</span><span class="sxs-lookup"><span data-stu-id="bef79-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="bef79-111">Ein Bezeichner für die Sicht.</span><span class="sxs-lookup"><span data-stu-id="bef79-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="bef79-112">Ein Zeiger auf die beste Route zum Ziel in dieser Ansicht.</span><span class="sxs-lookup"><span data-stu-id="bef79-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="bef79-113">Der Besitzer der optimalen Route in dieser Ansicht.</span><span class="sxs-lookup"><span data-stu-id="bef79-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="bef79-114">Flags, die der optimalen Route in dieser Ansicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bef79-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="bef79-115">Handle für alle Routen, die sich in der Ansicht in einem halte Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="bef79-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




