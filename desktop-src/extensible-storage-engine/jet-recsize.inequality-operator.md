---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE. Ungleichheits Operator'
title: JET_RECSIZE. Ungleichheits Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 724009d5f4e816a5613b2fb6344b0a5388dea819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349559"
---
# <a name="jet_recsizeinequality-operator"></a><span data-ttu-id="09ed8-103">JET_RECSIZE. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="09ed8-103">JET_RECSIZE.Inequality operator</span></span>

<span data-ttu-id="09ed8-104">Bestimmt, ob zwei angegebene Instanzen von JET_RECSIZE nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="09ed8-104">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span>

<span data-ttu-id="09ed8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09ed8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="09ed8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09ed8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09ed8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ed8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="09ed8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="09ed8-108">Parameters</span></span>

  - <span data-ttu-id="09ed8-109">LHS</span><span class="sxs-lookup"><span data-stu-id="09ed8-109">lhs</span></span>  
    <span data-ttu-id="09ed8-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="09ed8-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="09ed8-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="09ed8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="09ed8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="09ed8-112">rhs</span></span>  
    <span data-ttu-id="09ed8-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="09ed8-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="09ed8-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="09ed8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="09ed8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09ed8-115">Return value</span></span>

<span data-ttu-id="09ed8-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="09ed8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="09ed8-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="09ed8-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09ed8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09ed8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09ed8-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="09ed8-119">Reference</span></span>

[<span data-ttu-id="09ed8-120">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="09ed8-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="09ed8-121">Mitglieder JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="09ed8-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="09ed8-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="09ed8-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
