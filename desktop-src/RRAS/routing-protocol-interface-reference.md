---
title: Referenz zur Routing Protokoll Schnittstelle
description: In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routing Protokolls als benutzermodusdll verwendet werden.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routing-und RAS-Dienst RRAS, Routing Protokoll Schnittstelle, Referenz
- Routing Protokoll Schnittstelle RRAS, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856096"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="2fbaa-105">Referenz zur Routing Protokoll Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2fbaa-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="2fbaa-106">In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routing Protokolls als benutzermodusdll verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fbaa-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="2fbaa-107">MPR50 sollte in der Make-Datei für das Routing Protokoll definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2fbaa-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="2fbaa-108">Das **sizeof \_ -IP- \_ Bindungs (x)-** Makro berechnet die Größe einer [**IP- \_ Adapter \_ Bindungs \_ Informations**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) Struktur, die die Anzahl der IP-Adressen enthält, in Byte.</span><span class="sxs-lookup"><span data-stu-id="2fbaa-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="2fbaa-109">Diese Verweis Elemente werden in den folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="2fbaa-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="2fbaa-110">Routing Protokoll Schnittstellen-Funktionen</span><span class="sxs-lookup"><span data-stu-id="2fbaa-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="2fbaa-111">Routing Protokoll Schnittstellen Strukturen</span><span class="sxs-lookup"><span data-stu-id="2fbaa-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="2fbaa-112">Verwaltung von IPX-Dienst Tabellen</span><span class="sxs-lookup"><span data-stu-id="2fbaa-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




