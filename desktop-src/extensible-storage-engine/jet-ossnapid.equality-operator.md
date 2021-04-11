---
description: 'Weitere Informationen finden Sie hier: JET_OSSNAPID. Gleichheits Operator'
title: JET_OSSNAPID. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39513985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Equality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a0fcd5d1edba1a0c3d05fe2b1778741626832d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217552"
---
# <a name="jet_ossnapidequality-operator"></a><span data-ttu-id="69b33-103">JET_OSSNAPID. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="69b33-103">JET_OSSNAPID.Equality operator</span></span>

<span data-ttu-id="69b33-104">Bestimmt, ob zwei angegebene Instanzen von JET_OSSNAPID gleich sind.</span><span class="sxs-lookup"><span data-stu-id="69b33-104">Determines whether two specified instances of JET_OSSNAPID are equal.</span></span>

<span data-ttu-id="69b33-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69b33-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69b33-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69b33-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69b33-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b33-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="69b33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69b33-108">Parameters</span></span>

  - <span data-ttu-id="69b33-109">LHS</span><span class="sxs-lookup"><span data-stu-id="69b33-109">lhs</span></span>  
    <span data-ttu-id="69b33-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69b33-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="69b33-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="69b33-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="69b33-112">rhs</span><span class="sxs-lookup"><span data-stu-id="69b33-112">rhs</span></span>  
    <span data-ttu-id="69b33-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69b33-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="69b33-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="69b33-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="69b33-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69b33-115">Return value</span></span>

<span data-ttu-id="69b33-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="69b33-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="69b33-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="69b33-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69b33-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b33-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69b33-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="69b33-119">Reference</span></span>

[<span data-ttu-id="69b33-120">JET_OSSNAPID Struktur</span><span class="sxs-lookup"><span data-stu-id="69b33-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="69b33-121">Mitglieder JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="69b33-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="69b33-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="69b33-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
