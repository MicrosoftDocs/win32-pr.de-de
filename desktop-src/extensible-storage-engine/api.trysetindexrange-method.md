---
description: Weitere Informationen finden Sie in der API. trysetindexrange-Methode.
title: API. trysetindexrange-Methode
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760069"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="9e466-103">API. trysetindexrange-Methode</span><span class="sxs-lookup"><span data-stu-id="9e466-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="9e466-104">Schränkt die Menge der Indexeinträge, die der Cursor durchlaufen kann, mithilfe von jetmove zu denjenigen ein, die mit dem aktuellen Index Eintrag beginnen und mit dem Index Eintrag enden, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="9e466-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="9e466-105">Ein Suchschlüssel muss zuvor mithilfe von jetmakekey erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="9e466-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="9e466-106">Gibt "true" zurück, wenn der Index Bereich nicht leer ist, andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="9e466-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="9e466-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e466-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e466-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e466-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e466-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e466-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9e466-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e466-110">Parameters</span></span>

  - <span data-ttu-id="9e466-111">-sid</span><span class="sxs-lookup"><span data-stu-id="9e466-111">sesid</span></span>  
    <span data-ttu-id="9e466-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e466-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9e466-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9e466-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e466-114">TableID</span><span class="sxs-lookup"><span data-stu-id="9e466-114">tableid</span></span>  
    <span data-ttu-id="9e466-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e466-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9e466-116">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e466-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e466-117">grbit</span><span class="sxs-lookup"><span data-stu-id="9e466-117">grbit</span></span>  
    <span data-ttu-id="9e466-118">Typ: [Microsoft. ISAM. ESENT. Interop. setindexrangegrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9e466-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9e466-119">Seek-Option.</span><span class="sxs-lookup"><span data-stu-id="9e466-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9e466-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e466-120">Return value</span></span>

<span data-ttu-id="9e466-121">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="9e466-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="9e466-122">True, wenn die Suche erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9e466-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e466-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e466-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e466-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="9e466-124">Reference</span></span>

[<span data-ttu-id="9e466-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9e466-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9e466-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9e466-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9e466-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e466-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
