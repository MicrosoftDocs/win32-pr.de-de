---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Gleichheits Operator'
title: JET_THREADSTATS. Gleichheits Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356967"
---
# <a name="jet_threadstatsequality-operator"></a><span data-ttu-id="b3ea2-103">JET_THREADSTATS. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="b3ea2-103">JET_THREADSTATS.Equality operator</span></span>

<span data-ttu-id="b3ea2-104">Bestimmt, ob zwei angegebene Instanzen von JET_THREADSTATS gleich sind.</span><span class="sxs-lookup"><span data-stu-id="b3ea2-104">Determines whether two specified instances of JET_THREADSTATS are equal.</span></span>

<span data-ttu-id="b3ea2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3ea2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b3ea2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3ea2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ea2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ea2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b3ea2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3ea2-108">Parameters</span></span>

  - <span data-ttu-id="b3ea2-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b3ea2-109">lhs</span></span>  
    <span data-ttu-id="b3ea2-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b3ea2-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="b3ea2-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="b3ea2-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3ea2-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b3ea2-112">rhs</span></span>  
    <span data-ttu-id="b3ea2-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b3ea2-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="b3ea2-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="b3ea2-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b3ea2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3ea2-115">Return value</span></span>

<span data-ttu-id="b3ea2-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b3ea2-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b3ea2-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="b3ea2-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3ea2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3ea2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3ea2-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="b3ea2-119">Reference</span></span>

[<span data-ttu-id="b3ea2-120">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="b3ea2-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="b3ea2-121">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="b3ea2-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="b3ea2-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3ea2-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
