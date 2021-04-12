---
title: Routing eingehender Anforderungen
description: Die HTTP-Server-API verwaltet eine Routing Datenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391189"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="48658-103">Routing eingehender Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48658-103">Routing Incoming Requests</span></span>

<span data-ttu-id="48658-104">Die HTTP-Server-API verwaltet eine Routing Datenbank, um zu bestimmen, welche Anwendung eine eingehende Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="48658-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="48658-105">Die Routing Tabelle wird aus der Reservierungs Datenbank erstellt und enthält Reservierungs Einträge sowie aktuelle Registrierungen.</span><span class="sxs-lookup"><span data-stu-id="48658-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="48658-106">Wenn eine Registrierung oder Reservierung durchgeführt wird, wird Sie in den Bucket der Routing Datenbank eingefügt, der dem Hosttyp entspricht:</span><span class="sxs-lookup"><span data-stu-id="48658-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="48658-107">\+ : Port Registrierungen werden in den Bucket "starke Platzhalter" eingefügt.</span><span class="sxs-lookup"><span data-stu-id="48658-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="48658-108">Host: Port Registrierungen werden in den "expliziten" Bucket eingefügt.</span><span class="sxs-lookup"><span data-stu-id="48658-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="48658-109">IP: Port Registrierungen werden in den Bucket "IP-gebundene schwache Platzhalter" eingefügt.</span><span class="sxs-lookup"><span data-stu-id="48658-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="48658-110">\* : Port Registrierungen werden in den Bucket "schwache Platzhalter" eingefügt.</span><span class="sxs-lookup"><span data-stu-id="48658-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="48658-111">Diese Schritte beziehen sich auch auf den Auftrag, bei dem eingehende HTTP-Anforderungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="48658-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="48658-112">Die starken Platzhalter Reservierungen werden zuerst geprüft, dann wird die explizite Reservierung geprüft, gefolgt vom IP-gebundenen schwachen Platzhalter und dem schwachen Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="48658-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="48658-113">Die Suche wird beendet, wenn eine Entsprechung gefunden wird, damit Registrierungen in einem der verbleibenden Bucket nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="48658-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="48658-114">Der HTTP-Server-API-Routing Algorithmus sucht die beste Entsprechung für das [URLPrefix](urlprefix-strings.md) durch das Durchsuchen der Registrierungseinträge und der Reservierungs Einträge der Routing Datenbank, beginnend mit dem großen Platzhalter Bucket und endende mit dem schwachen Platzhalter Bucket.</span><span class="sxs-lookup"><span data-stu-id="48658-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="48658-115">Die beste Entsprechung innerhalb eines Bucket ist die längste Entsprechung im relativen URI-Teil des URLPrefix-Werts (vorausgesetzt eine genaue Entsprechung für den Host, den Port und die Schema Teile der URL).</span><span class="sxs-lookup"><span data-stu-id="48658-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="48658-116">Wenn eine Entsprechung in einem Bucket gefunden wird, beendet der Routing Algorithmus die Suche und überspringt alle Bucket mit niedrigerer Priorität.</span><span class="sxs-lookup"><span data-stu-id="48658-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="48658-117">Betrachten Sie z. b. die folgenden Registrierungen (in absteigender Reihenfolge der Priorität basierend auf Bucket-Typen aufgeführt):</span><span class="sxs-lookup"><span data-stu-id="48658-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="48658-118">Registrierung: `https://+:80/vroot/` wird von Anwendung 1 registriert</span><span class="sxs-lookup"><span data-stu-id="48658-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="48658-119">Registrierung: `https://adatum.com:80/` wird von Anwendung 2 registriert</span><span class="sxs-lookup"><span data-stu-id="48658-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="48658-120">Registrierung: `https://\*:80/` wird von Anwendung 3 registriert.</span><span class="sxs-lookup"><span data-stu-id="48658-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="48658-121">Eine eingehende Anforderung für `https://adatum.com:80/vroot/subdir/file.htm/` wird an Anwendung 1 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="48658-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="48658-122">Eine eingehende Anforderung für `https://adatum.com:80/default.htm/` wird an Anwendung 2 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="48658-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="48658-123">Eine eingehende Anforderung für `https://otheradatum.com:80/file.htm/` wird an Anwendung 3 übermittelt.</span><span class="sxs-lookup"><span data-stu-id="48658-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="48658-124">Wenn die beste Entsprechung ein Reservierungs Eintrag ist, bedeutet dies, dass die Anwendung, die die Anforderung empfangen sollte, nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48658-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="48658-125">Sehen Sie sich beispielsweise die folgende Registrierung und Reservierung an:</span><span class="sxs-lookup"><span data-stu-id="48658-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="48658-126">Registrierung: `https://\*:80/vroot/` wird von Anwendung 1 registriert, Benutzer A</span><span class="sxs-lookup"><span data-stu-id="48658-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="48658-127">Reservierung: wurde `https://adatum.com:80/` für Benutzer B reserviert.</span><span class="sxs-lookup"><span data-stu-id="48658-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="48658-128">Eine eingehende Anforderung für `https://adatum.com:80/vroot/file.htm/` wird nicht an Anwendung 1 übermittelt, da die beste Entsprechung zum Reservierungs Eintrag für Benutzer B führt. Die Rang Folge Regeln werden in diesem Fall auf die Reservierung angewendet, die eine höhere Priorität hat.</span><span class="sxs-lookup"><span data-stu-id="48658-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="48658-129">Wenn kein Prozess aktiv ist, der autorisiert und bei Dienst Anforderungen für die empfangene URL registriert ist, wird die Anforderung mit dem Statuscode 400 (ungültige Anforderung) zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="48658-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




