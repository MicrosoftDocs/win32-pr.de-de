---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Ungleichheits Operator'
title: JET_THREADSTATS. Ungleichheits Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510396
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dd3bc0f56b5fbbc47928387f999664df7bcc7a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867556"
---
# <a name="jet_threadstatsinequality-operator"></a><span data-ttu-id="ebc52-103">JET_THREADSTATS. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="ebc52-103">JET_THREADSTATS.Inequality operator</span></span>

<span data-ttu-id="ebc52-104">Bestimmt, ob zwei angegebene Instanzen von JET_THREADSTATS nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ebc52-104">Determines whether two specified instances of JET_THREADSTATS are not equal.</span></span>

<span data-ttu-id="ebc52-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebc52-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ebc52-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebc52-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc52-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebc52-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ebc52-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebc52-108">Parameters</span></span>

  - <span data-ttu-id="ebc52-109">LHS</span><span class="sxs-lookup"><span data-stu-id="ebc52-109">lhs</span></span>  
    <span data-ttu-id="ebc52-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ebc52-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="ebc52-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="ebc52-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebc52-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ebc52-112">rhs</span></span>  
    <span data-ttu-id="ebc52-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ebc52-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="ebc52-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="ebc52-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ebc52-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebc52-115">Return value</span></span>

<span data-ttu-id="ebc52-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ebc52-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ebc52-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ebc52-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ebc52-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebc52-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebc52-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="ebc52-119">Reference</span></span>

[<span data-ttu-id="ebc52-120">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="ebc52-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="ebc52-121">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="ebc52-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="ebc52-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="ebc52-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
