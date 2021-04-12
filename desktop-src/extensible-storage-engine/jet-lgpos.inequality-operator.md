---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. Ungleichheits Operator'
title: JET_LGPOS. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e324131591f1d6bee3c00e6260f31f6580ec086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960298"
---
# <a name="jet_lgposinequality-operator"></a><span data-ttu-id="39f55-103">JET_LGPOS. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="39f55-103">JET_LGPOS.Inequality operator</span></span>

<span data-ttu-id="39f55-104">Bestimmt, ob zwei angegebene Instanzen von JET_LGPOS nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="39f55-104">Determines whether two specified instances of JET_LGPOS are not equal.</span></span>

<span data-ttu-id="39f55-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39f55-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39f55-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="39f55-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39f55-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39f55-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="39f55-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39f55-108">Parameters</span></span>

  - <span data-ttu-id="39f55-109">LHS</span><span class="sxs-lookup"><span data-stu-id="39f55-109">lhs</span></span>  
    <span data-ttu-id="39f55-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="39f55-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="39f55-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="39f55-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="39f55-112">rhs</span><span class="sxs-lookup"><span data-stu-id="39f55-112">rhs</span></span>  
    <span data-ttu-id="39f55-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="39f55-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="39f55-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="39f55-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="39f55-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39f55-115">Return value</span></span>

<span data-ttu-id="39f55-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="39f55-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="39f55-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="39f55-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="39f55-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39f55-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39f55-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="39f55-119">Reference</span></span>

[<span data-ttu-id="39f55-120">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="39f55-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="39f55-121">Mitglieder JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="39f55-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="39f55-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="39f55-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
