---
description: 'Weitere Informationen finden Sie hier: JET_COMMIT_ID. LessThanOrEqual-Operator'
title: JET_COMMIT_ID. LessThanOrEqual-Operator (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104413
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 872ded299fc36295ea56500605f23af37feb0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757944"
---
# <a name="jet_commit_idlessthanorequal-operator"></a><span data-ttu-id="e2e10-103">JET_COMMIT_ID. LessThanOrEqual-Operator</span><span class="sxs-lookup"><span data-stu-id="e2e10-103">JET_COMMIT_ID.LessThanOrEqual operator</span></span>

<span data-ttu-id="e2e10-104">Stellen Sie fest, ob eine comentschärd vor einer anderen comentschärd ist.</span><span class="sxs-lookup"><span data-stu-id="e2e10-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="e2e10-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2e10-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e2e10-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2e10-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e10-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e10-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="e2e10-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e10-108">Parameters</span></span>

  - <span data-ttu-id="e2e10-109">LHS</span><span class="sxs-lookup"><span data-stu-id="e2e10-109">lhs</span></span>  
    <span data-ttu-id="e2e10-110">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="e2e10-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="e2e10-111">Die erste zu vergleichende comentschärd.</span><span class="sxs-lookup"><span data-stu-id="e2e10-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2e10-112">rhs</span><span class="sxs-lookup"><span data-stu-id="e2e10-112">rhs</span></span>  
    <span data-ttu-id="e2e10-113">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="e2e10-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="e2e10-114">Die zweite zu vergleichende comentschärd.</span><span class="sxs-lookup"><span data-stu-id="e2e10-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e2e10-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e10-115">Return value</span></span>

<span data-ttu-id="e2e10-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e2e10-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e2e10-117">True, wenn LHS vor oder gleich RHS ist.</span><span class="sxs-lookup"><span data-stu-id="e2e10-117">True if lhs comes before or equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2e10-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2e10-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2e10-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2e10-119">Reference</span></span>

[<span data-ttu-id="e2e10-120">JET_COMMIT_ID-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2e10-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="e2e10-121">Mitglieder JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="e2e10-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="e2e10-122">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2e10-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
