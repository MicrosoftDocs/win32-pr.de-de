---
description: 'Weitere Informationen finden Sie hier: JET_BKINFO. Gleichheits Operator'
title: JET_BKINFO. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a20cc09e55ce2bbb194561d4e371b81f9bcb2a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369793"
---
# <a name="jet_bkinfoequality-operator"></a><span data-ttu-id="7292a-103">JET_BKINFO. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="7292a-103">JET_BKINFO.Equality operator</span></span>

<span data-ttu-id="7292a-104">Bestimmt, ob zwei angegebene Instanzen von JET_BKINFO gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7292a-104">Determines whether two specified instances of JET_BKINFO are equal.</span></span>

<span data-ttu-id="7292a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7292a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7292a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7292a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7292a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7292a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7292a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7292a-108">Parameters</span></span>

  - <span data-ttu-id="7292a-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7292a-109">lhs</span></span>  
    <span data-ttu-id="7292a-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7292a-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="7292a-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7292a-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7292a-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7292a-112">rhs</span></span>  
    <span data-ttu-id="7292a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7292a-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="7292a-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7292a-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7292a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7292a-115">Return value</span></span>

<span data-ttu-id="7292a-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7292a-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7292a-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7292a-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7292a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7292a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7292a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="7292a-119">Reference</span></span>

[<span data-ttu-id="7292a-120">JET_BKINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="7292a-120">JET_BKINFO structure</span></span>](./jet-bkinfo-structure2.md)

[<span data-ttu-id="7292a-121">Mitglieder JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="7292a-121">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="7292a-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7292a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
