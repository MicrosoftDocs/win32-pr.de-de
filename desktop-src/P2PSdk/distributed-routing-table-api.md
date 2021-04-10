---
description: Mit der DRT-API (verteilte Routing Tabelle) können Anwendungen numerische Schlüssel in einem Peer Netzwerk veröffentlichen und auflösen.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: Verteiltes Routing Tabellen-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042269"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="d1510-103">Verteiltes Routing Tabellen-API</span><span class="sxs-lookup"><span data-stu-id="d1510-103">Distributed Routing Table API</span></span>

<span data-ttu-id="d1510-104">Mit der DRT-API (verteilte Routing Tabelle) können Anwendungen numerische Schlüssel in einem Peer Netzwerk veröffentlichen und auflösen.</span><span class="sxs-lookup"><span data-stu-id="d1510-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="d1510-105">Eine Anwendung, die DRT nutzt, kann folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="d1510-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="d1510-106">Erstellen Sie anwendungsspezifische verteilte Routing Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d1510-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="d1510-107">Registrieren Sie Schlüssel, und ordnen Sie diese Schlüssel IP-Adressen und Anwendungsdaten zu.</span><span class="sxs-lookup"><span data-stu-id="d1510-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="d1510-108">Suchen Sie nach Schlüsseln, und rufen Sie die zugeordneten IP-Adressen und Anwendungsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="d1510-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="d1510-109">Diese Funktion kann verwendet werden, um verteilte Hash Tabellen (dhts), Server lose namens Auflösungs Systeme und Überlagerungs Gitternetz Werken vieler Topologien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1510-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="d1510-110">Die Administratoren und Benutzer von DRT-fähigen Anwendungen sollten den Endbenutzern Ihrer Anwendungen die zu veröffentlichenden Informationen bewusst machen.</span><span class="sxs-lookup"><span data-stu-id="d1510-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="d1510-111">Microsoft-Server werden nicht von dieser Technologie verwendet, und die Informationen werden nicht an Microsoft gesendet.</span><span class="sxs-lookup"><span data-stu-id="d1510-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="d1510-112">Die bereitgestellte Dokumentation für diese API ist in drei Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="d1510-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="d1510-113">`Section`</span><span class="sxs-lookup"><span data-stu-id="d1510-113">Section</span></span>                                                                                | <span data-ttu-id="d1510-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1510-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1510-115">Informationen zu verteilten Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="d1510-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="d1510-116">Informationen, die den Lebenszyklus und die Zustandsänderungen der DRT-API beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d1510-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="d1510-117">Verwenden des Tabellen-API für verteilten Routing</span><span class="sxs-lookup"><span data-stu-id="d1510-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="d1510-118">Informationen, die die allgemeine Verwendung der DRT-API beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d1510-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="d1510-119">Tabellen-API Referenz zu verteiltem Routing</span><span class="sxs-lookup"><span data-stu-id="d1510-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="d1510-120">Informationen zu den Funktionen, Datenstrukturen und Enumerationskonstanten, die die DRT-API bilden.</span><span class="sxs-lookup"><span data-stu-id="d1510-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 




