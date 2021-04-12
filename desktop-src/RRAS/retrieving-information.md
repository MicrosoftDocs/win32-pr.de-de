---
title: Abrufen von Informationen
description: RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem bestimmten handle verwiesen wird, mithilfe der Funktionen rtmgetentityinfo, rtmgetdestinfo, rtmgetrouteinfo und rtmgetnexthopinfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206355"
---
# <a name="retrieving-information"></a><span data-ttu-id="2c20b-103">Abrufen von Informationen</span><span class="sxs-lookup"><span data-stu-id="2c20b-103">Retrieving Information</span></span>

<span data-ttu-id="2c20b-104">RTMv2 ermöglicht einem Client das Abrufen der Informationen, auf die von einem bestimmten handle verwiesen wird, mithilfe der Funktionen [**rtmgetentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**rtmgetdestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**rtmgetrouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)und [**rtmgetnexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="2c20b-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="2c20b-105">Diese Funktionsaufrufe verfügen über entsprechende Funktionen ([**rtmreleaseentityinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**rtmreleasedestinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**rtmreleaserouteinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**rtmreleasenexthopinfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)), um die Handles freizugeben, die mit der vom Routing Tabellen-Manager zurückgegebenen Informationsstruktur verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2c20b-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="2c20b-106">Informationen für Clients sind nur in der aktuellen Instanz und Adressfamilie verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c20b-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="2c20b-107">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Suchen nach der besten Route](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="2c20b-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="2c20b-108">Verwenden von rtmgetexactmatchroute und rtmgetexactmatchdestination</span><span class="sxs-lookup"><span data-stu-id="2c20b-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="2c20b-109">Die Funktionen [**rtmgetexactmatchroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) und [**rtmgetexactmatchdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) werden von Clients verwendet, um eine bestimmte Route oder ein bestimmtes Ziel zu finden.</span><span class="sxs-lookup"><span data-stu-id="2c20b-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="2c20b-110">Diese Funktionen sparen Zeit, indem Sie die vergleichsarbeit für den Client durcharbeiten.</span><span class="sxs-lookup"><span data-stu-id="2c20b-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="2c20b-111">Wenn z. b. RIP eine Route aktualisiert, muss RIP die alten metrikinformationen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="2c20b-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="2c20b-112">RIP sucht nach der Route und deren Informationen.</span><span class="sxs-lookup"><span data-stu-id="2c20b-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="2c20b-113">Anschließend kann RIP die Informationen kopieren und die Route aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c20b-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="2c20b-114">Verwenden von "rtmgetarstspecificdestination"</span><span class="sxs-lookup"><span data-stu-id="2c20b-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="2c20b-115">Mithilfe der Funktion [**rtmgetmuspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) wird das Ziel gefunden, das am besten mit dem angegebenen Netzwerk Präfix übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2c20b-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="2c20b-116">Beispielsweise verwendet der Multicast-Gruppen-Manager diese Funktion, um eine RPF-Überprüfung (reversepfad-Weiterleitung) für eine einzelne Adresse auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2c20b-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="2c20b-117">Die-Funktion kann auch verwendet werden, um den lokalen nächsten Hop für einen bestimmten Remote-Hop zu suchen.</span><span class="sxs-lookup"><span data-stu-id="2c20b-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="2c20b-118">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie untersuchen nach Routen mithilfe eines Präfix Baums](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) und [Suchen nach der besten Route](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="2c20b-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="2c20b-119">Verwenden von rtmgetlessspecificdestination</span><span class="sxs-lookup"><span data-stu-id="2c20b-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="2c20b-120">Die [**rtmgetlessspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) -Funktion wird verwendet, um das Ziel zu finden, das die nächstbeste Entsprechung für das angegebene Netzwerk Präfix ist.</span><span class="sxs-lookup"><span data-stu-id="2c20b-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="2c20b-121">Diese Funktion kann wiederholt aufgerufen werden, um die nächste nachfolgende weniger spezifische Treffer Rückgabe zurückzugeben, bis keine weiteren Ziele mehr gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2c20b-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="2c20b-122">Diese Funktion wird nach einem Aufruf von [**rtmgetarstspecificdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2c20b-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="2c20b-123">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie untersuchen nach Routen mithilfe eines Präfix Baums](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="2c20b-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="2c20b-124">Verwenden von rtmisbestroute</span><span class="sxs-lookup"><span data-stu-id="2c20b-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="2c20b-125">Die [**rtmisbestroute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) -Funktion ermöglicht es einem Client, schnell herauszufinden, ob eine bestimmte Route die beste Route zu einem Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="2c20b-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="2c20b-126">Beispielsweise muss ein Client möglicherweise nur eine bestimmte Route speichern, wenn er die beste Route ist.</span><span class="sxs-lookup"><span data-stu-id="2c20b-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="2c20b-127">Daher kann der Client diese Funktion anstelle von allen Routen auflisten und den Vergleich selbst durchführen.</span><span class="sxs-lookup"><span data-stu-id="2c20b-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




