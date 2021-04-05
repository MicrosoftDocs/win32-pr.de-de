---
description: 'Weitere Informationen finden Sie unter: JET_COMMIT_ID. GreaterThan-Operator'
title: JET_COMMIT_ID. GreaterThan-Operator (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 55104406
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfcb6cdc5a07cd4c114d5f61aaf597711636526b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757945"
---
# <a name="jet_commit_idgreaterthan-operator"></a><span data-ttu-id="baf9a-103">JET_COMMIT_ID. GreaterThan-Operator</span><span class="sxs-lookup"><span data-stu-id="baf9a-103">JET_COMMIT_ID.GreaterThan operator</span></span>

<span data-ttu-id="baf9a-104">Stellen Sie fest, ob eine comentschärd vor einer anderen comentschärd ist.</span><span class="sxs-lookup"><span data-stu-id="baf9a-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="baf9a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="baf9a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="baf9a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="baf9a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="baf9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="baf9a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="baf9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf9a-108">Parameters</span></span>

  - <span data-ttu-id="baf9a-109">LHS</span><span class="sxs-lookup"><span data-stu-id="baf9a-109">lhs</span></span>  
    <span data-ttu-id="baf9a-110">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="baf9a-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="baf9a-111">Die erste zu vergleichende comentschärd.</span><span class="sxs-lookup"><span data-stu-id="baf9a-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="baf9a-112">rhs</span><span class="sxs-lookup"><span data-stu-id="baf9a-112">rhs</span></span>  
    <span data-ttu-id="baf9a-113">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="baf9a-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="baf9a-114">Die zweite zu vergleichende comentschärd.</span><span class="sxs-lookup"><span data-stu-id="baf9a-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="baf9a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baf9a-115">Return value</span></span>

<span data-ttu-id="baf9a-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="baf9a-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="baf9a-117">True, wenn LHS hinter RHS steht.</span><span class="sxs-lookup"><span data-stu-id="baf9a-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="baf9a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baf9a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="baf9a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="baf9a-119">Reference</span></span>

[<span data-ttu-id="baf9a-120">JET_COMMIT_ID-Klasse</span><span class="sxs-lookup"><span data-stu-id="baf9a-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="baf9a-121">Mitglieder JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="baf9a-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="baf9a-122">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="baf9a-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
