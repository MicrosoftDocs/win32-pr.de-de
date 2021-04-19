---
description: 'Weitere Informationen finden Sie hier: API. jetgotoposition-Methode'
title: API. jetgotoposition-Methode
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5917e729d1a9ae5ae0a3715d6a2a2a81f45f75e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348243"
---
# <a name="apijetgotoposition-method"></a><span data-ttu-id="c5651-103">API. jetgotoposition-Methode</span><span class="sxs-lookup"><span data-stu-id="c5651-103">Api.JetGotoPosition method</span></span>

<span data-ttu-id="c5651-104">Verschiebt einen Cursor an eine neue Position, die ein Bruchteil der Art und Weise des aktuellen Indexes ist.</span><span class="sxs-lookup"><span data-stu-id="c5651-104">Moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="c5651-105">Siehe auch [jetgetrecordposition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="c5651-105">Also see [JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span></span>

<span data-ttu-id="c5651-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5651-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5651-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c5651-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5651-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5651-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="c5651-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5651-109">Parameters</span></span>

  - <span data-ttu-id="c5651-110">-sid</span><span class="sxs-lookup"><span data-stu-id="c5651-110">sesid</span></span>  
    <span data-ttu-id="c5651-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5651-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c5651-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c5651-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5651-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c5651-113">tableid</span></span>  
    <span data-ttu-id="c5651-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5651-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c5651-115">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5651-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5651-116">recpos</span><span class="sxs-lookup"><span data-stu-id="c5651-116">recpos</span></span>  
    <span data-ttu-id="c5651-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="c5651-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="c5651-118">Die ungefähre Position, zu der gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5651-118">The approximate position to move to.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5651-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5651-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5651-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="c5651-120">Reference</span></span>

[<span data-ttu-id="c5651-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5651-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c5651-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c5651-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c5651-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c5651-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
