---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. Gleichheits Operator'
title: JET_LGPOS. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510144
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdde1ee34cb60761d55dd52f2145a6b9bdd0a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362779"
---
# <a name="jet_lgposequality-operator"></a><span data-ttu-id="77fa1-103">JET_LGPOS. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="77fa1-103">JET_LGPOS.Equality operator</span></span>

<span data-ttu-id="77fa1-104">Bestimmt, ob zwei angegebene Instanzen von JET_LGPOS gleich sind.</span><span class="sxs-lookup"><span data-stu-id="77fa1-104">Determines whether two specified instances of JET_LGPOS are equal.</span></span>

<span data-ttu-id="77fa1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77fa1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77fa1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="77fa1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77fa1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="77fa1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="77fa1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="77fa1-108">Parameters</span></span>

  - <span data-ttu-id="77fa1-109">LHS</span><span class="sxs-lookup"><span data-stu-id="77fa1-109">lhs</span></span>  
    <span data-ttu-id="77fa1-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="77fa1-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="77fa1-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="77fa1-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="77fa1-112">rhs</span><span class="sxs-lookup"><span data-stu-id="77fa1-112">rhs</span></span>  
    <span data-ttu-id="77fa1-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="77fa1-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="77fa1-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="77fa1-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="77fa1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77fa1-115">Return value</span></span>

<span data-ttu-id="77fa1-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="77fa1-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="77fa1-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="77fa1-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="77fa1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77fa1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77fa1-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="77fa1-119">Reference</span></span>

[<span data-ttu-id="77fa1-120">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="77fa1-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="77fa1-121">Mitglieder JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="77fa1-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="77fa1-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="77fa1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
