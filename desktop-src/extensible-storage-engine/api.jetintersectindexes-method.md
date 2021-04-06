---
description: Weitere Informationen finden Sie in der API. jetintersectindexes-Methode.
title: API. jetintersectindexes-Methode
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960892"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="8b9bb-103">API. jetintersectindexes-Methode</span><span class="sxs-lookup"><span data-stu-id="8b9bb-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="8b9bb-104">Berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus unterschiedlichen sekundären Indizes für dieselbe Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="8b9bb-105">Dieser Vorgang ist nützlich, um die Gruppe von Datensätzen in einer Tabelle zu suchen, die mit zwei oder mehr Kriterien übereinstimmen, die mithilfe von Index Bereichen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="8b9bb-106">Siehe auch [intersectindexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b9bb-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="8b9bb-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b9bb-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9bb-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8b9bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b9bb-110">Parameters</span></span>

  - <span data-ttu-id="8b9bb-111">-sid</span><span class="sxs-lookup"><span data-stu-id="8b9bb-111">sesid</span></span>  
    <span data-ttu-id="8b9bb-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8b9bb-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8b9bb-114">ranges</span><span class="sxs-lookup"><span data-stu-id="8b9bb-114">ranges</span></span>  
    <span data-ttu-id="8b9bb-115">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8b9bb-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="8b9bb-116">Ein, der die zu Intersect Ende Index Bereiche ist.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-116">An the index ranges to intersect.</span></span> <span data-ttu-id="8b9bb-117">Für den TableIDs-Wert in den Bereichen müssen Index Bereiche festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="8b9bb-118">Verwenden Sie [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md) , um einen Index Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="8b9bb-119">numbereiche</span><span class="sxs-lookup"><span data-stu-id="8b9bb-119">numRanges</span></span>  
    <span data-ttu-id="8b9bb-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8b9bb-121">Die Anzahl der Index Bereiche.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="8b9bb-122">RecordList</span><span class="sxs-lookup"><span data-stu-id="8b9bb-122">recordlist</span></span>  
    <span data-ttu-id="8b9bb-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="8b9bb-124">Gibt Informationen über die temporäre Tabelle zurück, die die Überschneidungs Ergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="8b9bb-125">grbit</span><span class="sxs-lookup"><span data-stu-id="8b9bb-125">grbit</span></span>  
    <span data-ttu-id="8b9bb-126">Typ: [Microsoft. ISAM. ESENT. Interop. intersectindexesgrbit](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8b9bb-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8b9bb-127">Schnittstellen Optionen.</span><span class="sxs-lookup"><span data-stu-id="8b9bb-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b9bb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b9bb-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b9bb-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="8b9bb-129">Reference</span></span>

[<span data-ttu-id="8b9bb-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b9bb-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8b9bb-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8b9bb-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8b9bb-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8b9bb-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
