---
description: Weitere Informationen finden Sie in der API. intersectindexes-Methode.
title: API. intersectindexes-Methode
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524776"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="8cc70-103">API. intersectindexes-Methode</span><span class="sxs-lookup"><span data-stu-id="8cc70-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="8cc70-104">Intersect eine Gruppe von Index Bereichen und gibt die Lesezeichen der Datensätze zurück, die in allen Index Bereichen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8cc70-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="8cc70-105">Siehe auch [jetintersectindexes (JET_SESID, \[ \] , Int32, JET_RECORDLIST, intersectindexesgrbit)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="8cc70-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="8cc70-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8cc70-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8cc70-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8cc70-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc70-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc70-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="8cc70-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cc70-109">Parameters</span></span>

  - <span data-ttu-id="8cc70-110">-sid</span><span class="sxs-lookup"><span data-stu-id="8cc70-110">sesid</span></span>  
    <span data-ttu-id="8cc70-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8cc70-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8cc70-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8cc70-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8cc70-113">tableids</span><span class="sxs-lookup"><span data-stu-id="8cc70-113">tableids</span></span>  
    <span data-ttu-id="8cc70-114">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8cc70-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="8cc70-115">Das zu verwendende TableIDs.</span><span class="sxs-lookup"><span data-stu-id="8cc70-115">The tableids to use.</span></span> <span data-ttu-id="8cc70-116">Jede TableID muss von einem anderen Index für dieselbe Tabelle sein und über einen aktiven Index Bereich verfügen.</span><span class="sxs-lookup"><span data-stu-id="8cc70-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="8cc70-117">Verwenden Sie [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md) , um einen Index Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cc70-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8cc70-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cc70-118">Return value</span></span>

<span data-ttu-id="8cc70-119">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="8cc70-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="8cc70-120">Die Lesezeichen der Datensätze, die in allen Index Bereichen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8cc70-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="8cc70-121">Die Lesezeichen werden in der Primärschlüssel Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8cc70-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8cc70-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc70-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cc70-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="8cc70-123">Reference</span></span>

[<span data-ttu-id="8cc70-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8cc70-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8cc70-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8cc70-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8cc70-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cc70-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
