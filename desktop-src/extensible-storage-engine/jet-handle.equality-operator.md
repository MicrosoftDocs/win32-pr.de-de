---
description: 'Weitere Informationen finden Sie hier: JET_HANDLE. Gleichheits Operator'
title: JET_HANDLE. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512271
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f0a7f10dd757a51dcdd450db2d2f0e863ab043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759600"
---
# <a name="jet_handleequality-operator"></a><span data-ttu-id="83fc9-103">JET_HANDLE. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="83fc9-103">JET_HANDLE.Equality operator</span></span>

<span data-ttu-id="83fc9-104">Bestimmt, ob zwei angegebene Instanzen von JET_HANDLE gleich sind.</span><span class="sxs-lookup"><span data-stu-id="83fc9-104">Determines whether two specified instances of JET_HANDLE are equal.</span></span>

<span data-ttu-id="83fc9-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="83fc9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="83fc9-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="83fc9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="83fc9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fc9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="83fc9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83fc9-108">Parameters</span></span>

  - <span data-ttu-id="83fc9-109">LHS</span><span class="sxs-lookup"><span data-stu-id="83fc9-109">lhs</span></span>  
    <span data-ttu-id="83fc9-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="83fc9-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="83fc9-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="83fc9-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="83fc9-112">rhs</span><span class="sxs-lookup"><span data-stu-id="83fc9-112">rhs</span></span>  
    <span data-ttu-id="83fc9-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="83fc9-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="83fc9-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="83fc9-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83fc9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83fc9-115">Return value</span></span>

<span data-ttu-id="83fc9-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="83fc9-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="83fc9-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="83fc9-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83fc9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83fc9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83fc9-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="83fc9-119">Reference</span></span>

[<span data-ttu-id="83fc9-120">JET_HANDLE Struktur</span><span class="sxs-lookup"><span data-stu-id="83fc9-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="83fc9-121">Mitglieder JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="83fc9-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="83fc9-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="83fc9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
