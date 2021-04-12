---
description: Weitere Informationen finden Sie in der API. resetindexrange-Methode.
title: API. resetindexrange-Methode
TOCTitle: 'ResetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.ResetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.resetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100832
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.ResetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 434740a549fa83d4601bf88ab09f307f4d19f189
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218653"
---
# <a name="apiresetindexrange-method"></a><span data-ttu-id="c1a65-103">API. resetindexrange-Methode</span><span class="sxs-lookup"><span data-stu-id="c1a65-103">Api.ResetIndexRange method</span></span>

<span data-ttu-id="c1a65-104">Entfernt einen Index Bereich, der mit [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md) oder [trysetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.trysetindexrange-method.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1a65-104">Removes an index range created with [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) or [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span> <span data-ttu-id="c1a65-105">Wenn kein Index Bereich vorhanden ist, führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="c1a65-105">If no index range is present this method does nothing.</span></span>

<span data-ttu-id="c1a65-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1a65-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1a65-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c1a65-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a65-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1a65-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub ResetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.ResetIndexRange(sesid, tableid)
```

``` csharp
public static void ResetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="c1a65-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1a65-109">Parameters</span></span>

  - <span data-ttu-id="c1a65-110">-sid</span><span class="sxs-lookup"><span data-stu-id="c1a65-110">sesid</span></span>  
    <span data-ttu-id="c1a65-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1a65-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c1a65-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c1a65-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1a65-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c1a65-113">tableid</span></span>  
    <span data-ttu-id="c1a65-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1a65-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c1a65-115">Der Cursor, auf dem der Index Bereich entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1a65-115">The cursor to remove the index range on.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1a65-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1a65-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1a65-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="c1a65-117">Reference</span></span>

[<span data-ttu-id="c1a65-118">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c1a65-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c1a65-119">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c1a65-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c1a65-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1a65-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
