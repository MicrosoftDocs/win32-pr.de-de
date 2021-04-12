---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Ungleichheits Operator'
title: JET_INSTANCE. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d537b01d3485e7f5e2d1d629c005a228eac92306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132053"
---
# <a name="jet_instanceinequality-operator"></a><span data-ttu-id="66a5d-103">JET_INSTANCE. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="66a5d-103">JET_INSTANCE.Inequality operator</span></span>

<span data-ttu-id="66a5d-104">Bestimmt, ob zwei angegebene Instanzen von JET_INSTANCE nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="66a5d-104">Determines whether two specified instances of JET_INSTANCE are not equal.</span></span>

<span data-ttu-id="66a5d-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66a5d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66a5d-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66a5d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66a5d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a5d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="66a5d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a5d-108">Parameters</span></span>

  - <span data-ttu-id="66a5d-109">LHS</span><span class="sxs-lookup"><span data-stu-id="66a5d-109">lhs</span></span>  
    <span data-ttu-id="66a5d-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66a5d-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="66a5d-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="66a5d-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="66a5d-112">rhs</span><span class="sxs-lookup"><span data-stu-id="66a5d-112">rhs</span></span>  
    <span data-ttu-id="66a5d-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66a5d-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="66a5d-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="66a5d-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="66a5d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66a5d-115">Return value</span></span>

<span data-ttu-id="66a5d-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="66a5d-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="66a5d-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="66a5d-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66a5d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66a5d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66a5d-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="66a5d-119">Reference</span></span>

[<span data-ttu-id="66a5d-120">JET_INSTANCE Struktur</span><span class="sxs-lookup"><span data-stu-id="66a5d-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="66a5d-121">Mitglieder JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="66a5d-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="66a5d-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="66a5d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
