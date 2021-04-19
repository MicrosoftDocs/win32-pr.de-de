---
description: 'Weitere Informationen finden Sie hier: JET_BKLOGTIME. Ungleichheits Operator'
title: JET_BKLOGTIME. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350884"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="437fe-103">JET_BKLOGTIME. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="437fe-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="437fe-104">Bestimmt, ob zwei angegebene Instanzen von JET_BKLOGTIME nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="437fe-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="437fe-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="437fe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="437fe-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="437fe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="437fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="437fe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="437fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="437fe-108">Parameters</span></span>

  - <span data-ttu-id="437fe-109">LHS</span><span class="sxs-lookup"><span data-stu-id="437fe-109">lhs</span></span>  
    <span data-ttu-id="437fe-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="437fe-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="437fe-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="437fe-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="437fe-112">rhs</span><span class="sxs-lookup"><span data-stu-id="437fe-112">rhs</span></span>  
    <span data-ttu-id="437fe-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="437fe-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="437fe-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="437fe-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="437fe-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="437fe-115">Return value</span></span>

<span data-ttu-id="437fe-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="437fe-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="437fe-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="437fe-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="437fe-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="437fe-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="437fe-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="437fe-119">Reference</span></span>

[<span data-ttu-id="437fe-120">JET_BKLOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="437fe-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="437fe-121">Mitglieder JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="437fe-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="437fe-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="437fe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
