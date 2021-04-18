---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Gleichheits Operator'
title: JET_INSTANCE. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41a3ffe2eebeb7566d431c655a27360c9380413c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347408"
---
# <a name="jet_instanceequality-operator"></a><span data-ttu-id="e24ea-103">JET_INSTANCE. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="e24ea-103">JET_INSTANCE.Equality operator</span></span>

<span data-ttu-id="e24ea-104">Bestimmt, ob zwei angegebene Instanzen von JET_INSTANCE gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e24ea-104">Determines whether two specified instances of JET_INSTANCE are equal.</span></span>

<span data-ttu-id="e24ea-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e24ea-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e24ea-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e24ea-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e24ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e24ea-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="e24ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e24ea-108">Parameters</span></span>

  - <span data-ttu-id="e24ea-109">LHS</span><span class="sxs-lookup"><span data-stu-id="e24ea-109">lhs</span></span>  
    <span data-ttu-id="e24ea-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e24ea-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e24ea-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="e24ea-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="e24ea-112">rhs</span><span class="sxs-lookup"><span data-stu-id="e24ea-112">rhs</span></span>  
    <span data-ttu-id="e24ea-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e24ea-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e24ea-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="e24ea-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e24ea-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e24ea-115">Return value</span></span>

<span data-ttu-id="e24ea-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e24ea-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e24ea-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e24ea-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e24ea-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e24ea-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e24ea-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e24ea-119">Reference</span></span>

[<span data-ttu-id="e24ea-120">JET_INSTANCE Struktur</span><span class="sxs-lookup"><span data-stu-id="e24ea-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="e24ea-121">Mitglieder JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e24ea-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="e24ea-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e24ea-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
