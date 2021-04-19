---
title: Sortieren (ADSI)
description: Ein Client kann einen Server zum Sortieren des Resultsets anfordern.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106341500"
---
# <a name="sorting-adsi"></a><span data-ttu-id="807bb-103">Sortieren (ADSI)</span><span class="sxs-lookup"><span data-stu-id="807bb-103">Sorting (ADSI)</span></span>

<span data-ttu-id="807bb-104">Ein Client kann einen Server zum Sortieren des Resultsets anfordern.</span><span class="sxs-lookup"><span data-stu-id="807bb-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="807bb-105">Sie können Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="807bb-105">You can specify:</span></span>

-   <span data-ttu-id="807bb-106">Sortierreihenfolge: entweder eine aufsteigende oder absteigende Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="807bb-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="807bb-107">Sortier Attribute: in einer Sortier Zeichenfolge können mehrere Attribute angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="807bb-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="807bb-108">Sortieren Sie z. b. nach Nachname und Vorname.</span><span class="sxs-lookup"><span data-stu-id="807bb-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="807bb-109">Wenn Sie die Sortierreihenfolge angeben, sollten Sie versuchen, eines der indizierten Attribute zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="807bb-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="807bb-110">Andernfalls muss der Server ein vervollständigen-Resultset berechnen, bevor es an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="807bb-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="807bb-111">Dies gilt auch, wenn Sie eine seitenweise Suche angefordert und eine Seitengröße angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="807bb-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="807bb-112">Nicht alle Verzeichnisserver unterstützen mehrere Attribut Sortierungen oder eine Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="807bb-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




