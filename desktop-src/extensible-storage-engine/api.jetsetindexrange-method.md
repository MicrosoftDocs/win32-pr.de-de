---
description: Weitere Informationen finden Sie in der API. jetsetindexrange-Methode.
title: API. jetsetindexrange-Methode
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041652"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="fcdc6-103">API. jetsetindexrange-Methode</span><span class="sxs-lookup"><span data-stu-id="fcdc6-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="fcdc6-104">Schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von [jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="fcdc6-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="fcdc6-105">Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey (JET_SESID, JET_TABLEID, \[ \] , Int32, makekeygrbit)](./api.jetmakekey-method.md)erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="fcdc6-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="fcdc6-106">Siehe auch [trysetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="fcdc6-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="fcdc6-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fcdc6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fcdc6-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fcdc6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fcdc6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcdc6-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fcdc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcdc6-110">Parameters</span></span>

  - <span data-ttu-id="fcdc6-111">-sid</span><span class="sxs-lookup"><span data-stu-id="fcdc6-111">sesid</span></span>  
    <span data-ttu-id="fcdc6-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fcdc6-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fcdc6-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fcdc6-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fcdc6-114">TableID</span><span class="sxs-lookup"><span data-stu-id="fcdc6-114">tableid</span></span>  
    <span data-ttu-id="fcdc6-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fcdc6-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fcdc6-116">Der Cursor, für den der Index Bereich festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcdc6-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="fcdc6-117">grbit</span><span class="sxs-lookup"><span data-stu-id="fcdc6-117">grbit</span></span>  
    <span data-ttu-id="fcdc6-118">Typ: [Microsoft. ISAM. ESENT. Interop. setindexrangegrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fcdc6-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fcdc6-119">Index Bereichs Optionen.</span><span class="sxs-lookup"><span data-stu-id="fcdc6-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcdc6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcdc6-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fcdc6-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="fcdc6-121">Reference</span></span>

[<span data-ttu-id="fcdc6-122">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="fcdc6-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fcdc6-123">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="fcdc6-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fcdc6-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcdc6-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
