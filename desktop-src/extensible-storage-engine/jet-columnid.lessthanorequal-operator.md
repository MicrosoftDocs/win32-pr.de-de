---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID. LessThanOrEqual-Operator'
title: JET_COLUMNID. LessThanOrEqual-Operator
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39513688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d6f98c5861a57fa4916ebca1b421c538d752d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753264"
---
# <a name="jet_columnidlessthanorequal-operator"></a><span data-ttu-id="0769a-103">JET_COLUMNID. LessThanOrEqual-Operator</span><span class="sxs-lookup"><span data-stu-id="0769a-103">JET_COLUMNID.LessThanOrEqual operator</span></span>

<span data-ttu-id="0769a-104">Bestimmen Sie, ob ein ColumnID vor oder gleich einem anderen ColumnID ist.</span><span class="sxs-lookup"><span data-stu-id="0769a-104">Determine whether one columnid is before or equal to another columnid.</span></span>

<span data-ttu-id="0769a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0769a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0769a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0769a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0769a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0769a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="0769a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0769a-108">Parameters</span></span>

  - <span data-ttu-id="0769a-109">LHS</span><span class="sxs-lookup"><span data-stu-id="0769a-109">lhs</span></span>  
    <span data-ttu-id="0769a-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0769a-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="0769a-111">Das erste zu vergleichende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="0769a-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="0769a-112">rhs</span><span class="sxs-lookup"><span data-stu-id="0769a-112">rhs</span></span>  
    <span data-ttu-id="0769a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0769a-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="0769a-114">Das zweite zu vergleichende ColumnID.</span><span class="sxs-lookup"><span data-stu-id="0769a-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0769a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0769a-115">Return value</span></span>

<span data-ttu-id="0769a-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0769a-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0769a-117">True, wenn LHS vor oder gleich RHS ist.</span><span class="sxs-lookup"><span data-stu-id="0769a-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0769a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0769a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0769a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="0769a-119">Reference</span></span>

[<span data-ttu-id="0769a-120">JET_COLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="0769a-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="0769a-121">Mitglieder JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="0769a-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="0769a-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0769a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
