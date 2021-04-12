---
description: 'Weitere Informationen finden Sie hier: JET_LS. Gleichheits Operator'
title: JET_LS. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516469
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equality
- Microsoft.Isam.Esent.Interop.JET_LS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ea1845d8146248e85df4b9a9aff79d845024b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217067"
---
# <a name="jet_lsequality-operator"></a><span data-ttu-id="d7a8e-103">JET_LS. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="d7a8e-103">JET_LS.Equality operator</span></span>

<span data-ttu-id="d7a8e-104">Bestimmt, ob zwei angegebene Instanzen von JET_LS gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d7a8e-104">Determines whether two specified instances of JET_LS are equal.</span></span>

<span data-ttu-id="d7a8e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d7a8e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d7a8e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d7a8e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a8e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7a8e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LS, _
    rhs As JET_LS _
) As Boolean
'Usage
Dim lhs As JET_LS
Dim rhs As JET_LS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LS lhs,
    JET_LS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="d7a8e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7a8e-108">Parameters</span></span>

  - <span data-ttu-id="d7a8e-109">LHS</span><span class="sxs-lookup"><span data-stu-id="d7a8e-109">lhs</span></span>  
    <span data-ttu-id="d7a8e-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d7a8e-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="d7a8e-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="d7a8e-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="d7a8e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="d7a8e-112">rhs</span></span>  
    <span data-ttu-id="d7a8e-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d7a8e-113">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="d7a8e-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="d7a8e-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d7a8e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7a8e-115">Return value</span></span>

<span data-ttu-id="d7a8e-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d7a8e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d7a8e-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d7a8e-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d7a8e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7a8e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d7a8e-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="d7a8e-119">Reference</span></span>

[<span data-ttu-id="d7a8e-120">JET_LS Struktur</span><span class="sxs-lookup"><span data-stu-id="d7a8e-120">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="d7a8e-121">Mitglieder JET_LS</span><span class="sxs-lookup"><span data-stu-id="d7a8e-121">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="d7a8e-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7a8e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
