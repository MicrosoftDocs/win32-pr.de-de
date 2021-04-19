---
description: Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Rowset-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346280"
---
# <a name="rowset-properties"></a><span data-ttu-id="cc88c-103">Rowset-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc88c-103">Rowset Properties</span></span>

<span data-ttu-id="cc88c-104">Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cc88c-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="cc88c-105">Zusätzlich zu den standardmäßigen OLE-DB-Rowseteigenschaften bietet Windows Search SQL die folgenden vier benutzerdefinierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc88c-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="cc88c-106">Die GUID für diesen Eigenschaften Satz ist {AA6EE6B0E828-11D0-B23E-00aa0047fc01}.</span><span class="sxs-lookup"><span data-stu-id="cc88c-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="cc88c-107">Windows Search unterstützt die Standard-OLE-DB-Eigenschaft DBPROP \_ CommandTimeout der Eigenschaften Gruppe [DBPROPSET- \_ Rowset](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cc88c-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="cc88c-108">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="cc88c-108">Property name</span></span>                  | <span data-ttu-id="cc88c-109">PROPID/Typ</span><span class="sxs-lookup"><span data-stu-id="cc88c-109">PROPID/type</span></span> | <span data-ttu-id="cc88c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc88c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc88c-111">Donotcomputeexpensive-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc88c-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="cc88c-112">15/VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="cc88c-112">15/VT\_BOOL</span></span> | <span data-ttu-id="cc88c-113">Wenn diese Eigenschaft auf true festgelegt wird, werden teure Eigenschaften wie gefundene Ergebnisse und der maximale Rang, bei denen die gesamte Abfrage ausgewertet werden muss, beim Zugriff auf eine Rowseteigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc88c-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="cc88c-114">Maximaler Rang (max. \_ Rang)</span><span class="sxs-lookup"><span data-stu-id="cc88c-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="cc88c-115">6/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cc88c-115">6/VT\_I4</span></span>    | <span data-ttu-id="cc88c-116">Der höchste Rang, der für jedes Ergebnis berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc88c-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cc88c-117">Gefundene Ergebnisse (Ergebnisse \_ gefunden)</span><span class="sxs-lookup"><span data-stu-id="cc88c-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="cc88c-118">7/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cc88c-118">7/VT\_I4</span></span>    | <span data-ttu-id="cc88c-119">Die Gesamtanzahl der eindeutigen Elemente für diese Abfrage.</span><span class="sxs-lookup"><span data-stu-id="cc88c-119">The total number of unique items for this query.</span></span> <span data-ttu-id="cc88c-120">Bei einer SELECT-Abfrage ist dies die Anzahl der Elemente im Rowset.</span><span class="sxs-lookup"><span data-stu-id="cc88c-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="cc88c-121">Bei einer Gruppe bei der Abfrage ist dies die Anzahl eindeutiger Blatt Elemente.</span><span class="sxs-lookup"><span data-stu-id="cc88c-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="cc88c-122">Diese Eigenschaft identifiziert nicht die Anzahl der Zeilen im Rowset der obersten Ebene (die Anzahl der Gruppen der obersten Ebene).</span><span class="sxs-lookup"><span data-stu-id="cc88c-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="cc88c-123">Where-ID (whereid)</span><span class="sxs-lookup"><span data-stu-id="cc88c-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="cc88c-124">8/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cc88c-124">8/VT\_I4</span></span>    | <span data-ttu-id="cc88c-125">Der Bezeichner für die Einschränkungen, die für eine Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc88c-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="cc88c-126">Wenn ein Rowset geöffnet ist, wenn eine neue Abfrage ausgeführt wird, kann die neue Abfrage die Einschränkungen der älteren Abfrage wieder verwenden und so die bereits abgeschlossenen Arbeiten nutzen.</span><span class="sxs-lookup"><span data-stu-id="cc88c-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="cc88c-127">Weitere Informationen zur Verwendung von WHERE-Einschränkungen finden Sie in der [reusewhere-Funktion](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="cc88c-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cc88c-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc88c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc88c-129">Indizieren von Priorisierungs-und rowsetereignissen in Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc88c-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
