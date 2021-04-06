---
description: 'Weitere Informationen finden Sie hier: JET_INDEXID. Gleichheits Operator'
title: JET_INDEXID. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fa7574aeed52377b516f63549a6f690dc168d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960965"
---
# <a name="jet_indexidequality-operator"></a><span data-ttu-id="ff8f7-103">JET_INDEXID. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="ff8f7-103">JET_INDEXID.Equality operator</span></span>

<span data-ttu-id="ff8f7-104">Bestimmt, ob zwei angegebene Instanzen von JET_INDEXID gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ff8f7-104">Determines whether two specified instances of JET_INDEXID are equal.</span></span>

<span data-ttu-id="ff8f7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff8f7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff8f7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff8f7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff8f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff8f7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ff8f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff8f7-108">Parameters</span></span>

  - <span data-ttu-id="ff8f7-109">LHS</span><span class="sxs-lookup"><span data-stu-id="ff8f7-109">lhs</span></span>  
    <span data-ttu-id="ff8f7-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ff8f7-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="ff8f7-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="ff8f7-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff8f7-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ff8f7-112">rhs</span></span>  
    <span data-ttu-id="ff8f7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ff8f7-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="ff8f7-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="ff8f7-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ff8f7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff8f7-115">Return value</span></span>

<span data-ttu-id="ff8f7-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ff8f7-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ff8f7-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ff8f7-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff8f7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff8f7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff8f7-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="ff8f7-119">Reference</span></span>

[<span data-ttu-id="ff8f7-120">JET_INDEXID Struktur</span><span class="sxs-lookup"><span data-stu-id="ff8f7-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="ff8f7-121">Mitglieder JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="ff8f7-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="ff8f7-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff8f7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
