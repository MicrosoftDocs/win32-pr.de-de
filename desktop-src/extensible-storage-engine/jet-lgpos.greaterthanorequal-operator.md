---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. GreaterThanOrEqual-Operator'
title: JET_LGPOS. GreaterThanOrEqual-Operator
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a932ea983b3044d1db8395fbf87962cd3b733ae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351160"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a><span data-ttu-id="5837d-103">JET_LGPOS. GreaterThanOrEqual-Operator</span><span class="sxs-lookup"><span data-stu-id="5837d-103">JET_LGPOS.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="5837d-104">Bestimmen Sie, ob eine Protokoll Position nach oder gleich einer anderen Protokoll Position ist.</span><span class="sxs-lookup"><span data-stu-id="5837d-104">Determine whether one log position is after or equal to another log position.</span></span>

<span data-ttu-id="5837d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5837d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5837d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5837d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5837d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5837d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="5837d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5837d-108">Parameters</span></span>

  - <span data-ttu-id="5837d-109">LHS</span><span class="sxs-lookup"><span data-stu-id="5837d-109">lhs</span></span>  
    <span data-ttu-id="5837d-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5837d-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="5837d-111">Die erste zu vergleichende Protokoll Position.</span><span class="sxs-lookup"><span data-stu-id="5837d-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="5837d-112">rhs</span><span class="sxs-lookup"><span data-stu-id="5837d-112">rhs</span></span>  
    <span data-ttu-id="5837d-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5837d-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="5837d-114">Die zweite Protokoll Position, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5837d-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5837d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5837d-115">Return value</span></span>

<span data-ttu-id="5837d-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5837d-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="5837d-117">True, wenn LHS nach oder gleich RHS ist.</span><span class="sxs-lookup"><span data-stu-id="5837d-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5837d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5837d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5837d-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="5837d-119">Reference</span></span>

[<span data-ttu-id="5837d-120">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="5837d-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="5837d-121">Mitglieder JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="5837d-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="5837d-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5837d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
