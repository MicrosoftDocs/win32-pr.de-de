---
title: Zwischenspeichern des Ergebnisses (Client seitig)
description: Das Client seitige Zwischenspeichern speichert das Resultset im Client Speicher und bietet Leistungsverbesserungen für die Clientseite.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Zwischenspeichern des Ergebnisses (Client seitig) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947355"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="a678a-104">Zwischenspeichern des Ergebnisses (Client seitig)</span><span class="sxs-lookup"><span data-stu-id="a678a-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="a678a-105">Das Client seitige Zwischenspeichern speichert das Resultset im Client Speicher und bietet Leistungsverbesserungen für die Clientseite.</span><span class="sxs-lookup"><span data-stu-id="a678a-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="a678a-106">Ein Client kann ein Objekt wiederholt ohne mehrere Fahrten zum Server erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a678a-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="a678a-107">Standardmäßig speichert ADSI das Resultset für die Clients zwischen.</span><span class="sxs-lookup"><span data-stu-id="a678a-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="a678a-108">Dadurch kann ADSI Clients die SQL-ähnliche Cursor Unterstützung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a678a-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="a678a-109">Sie können ein bestimmtes Resultset mehrmals durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a678a-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="a678a-110">Mit ADSI können Clients den Cache auch deaktivieren, um die Arbeitsspeicher Anforderungen zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a678a-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="a678a-111">Wenn das Client seitige Zwischenspeichern deaktiviert ist, behält der Client das Resultset nicht im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a678a-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="a678a-112">Jede Zeile wird freigegeben, nachdem Sie von der Anwendung abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a678a-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="a678a-113">Die Deaktivierung der Client seitigen Zwischenspeicherung kann nützlich sein, um die Client seitigen Speicheranforderungen in Fällen zu verringern, in denen Sie nur einen einzigen Durchlauf durch das Resultset durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="a678a-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="a678a-114">Wenn Clients das Ergebnis jedoch nicht zwischenspeichern, erhalten Sie Cursor Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="a678a-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="a678a-115">Weitere Informationen zum Zwischenspeichern von Ergebnissen mit einer bestimmten Suchschnittstelle finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a678a-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="a678a-116">Ergebnis Zwischenspeicherung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="a678a-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="a678a-117">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="a678a-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="a678a-118">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="a678a-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




