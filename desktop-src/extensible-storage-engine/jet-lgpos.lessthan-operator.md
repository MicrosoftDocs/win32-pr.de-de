---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. LessThan-Operator'
title: JET_LGPOS. LessThan-Operator
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThan(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39510335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.LessThan
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_LessThan
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ec121f9d13686d3d5c8ad22aa0fb3aed8562b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346988"
---
# <a name="jet_lgposlessthan-operator"></a><span data-ttu-id="54c73-103">JET_LGPOS. LessThan-Operator</span><span class="sxs-lookup"><span data-stu-id="54c73-103">JET_LGPOS.LessThan operator</span></span>

<span data-ttu-id="54c73-104">Bestimmen Sie, ob eine Protokoll Position vor einer anderen Protokoll Position liegt.</span><span class="sxs-lookup"><span data-stu-id="54c73-104">Determine whether one log position is before another log position.</span></span>

<span data-ttu-id="54c73-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54c73-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54c73-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54c73-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54c73-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54c73-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="54c73-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54c73-108">Parameters</span></span>

  - <span data-ttu-id="54c73-109">LHS</span><span class="sxs-lookup"><span data-stu-id="54c73-109">lhs</span></span>  
    <span data-ttu-id="54c73-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="54c73-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="54c73-111">Die erste zu vergleichende Protokoll Position.</span><span class="sxs-lookup"><span data-stu-id="54c73-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="54c73-112">rhs</span><span class="sxs-lookup"><span data-stu-id="54c73-112">rhs</span></span>  
    <span data-ttu-id="54c73-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="54c73-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="54c73-114">Die zweite Protokoll Position, die verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="54c73-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="54c73-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54c73-115">Return value</span></span>

<span data-ttu-id="54c73-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="54c73-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="54c73-117">True, wenn LHS vor RHS steht.</span><span class="sxs-lookup"><span data-stu-id="54c73-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54c73-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c73-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54c73-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="54c73-119">Reference</span></span>

[<span data-ttu-id="54c73-120">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="54c73-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="54c73-121">Mitglieder JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="54c73-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="54c73-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="54c73-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
