---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID. Gleichheits Operator'
title: JET_COLUMNID. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514850
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79d6d376d9a574587e5e3fc5329a7c092da73a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348839"
---
# <a name="jet_columnidequality-operator"></a><span data-ttu-id="4ac29-103">JET_COLUMNID. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="4ac29-103">JET_COLUMNID.Equality operator</span></span>

<span data-ttu-id="4ac29-104">Bestimmt, ob zwei angegebene Instanzen von JET_COLUMNID gleich sind.</span><span class="sxs-lookup"><span data-stu-id="4ac29-104">Determines whether two specified instances of JET_COLUMNID are equal.</span></span>

<span data-ttu-id="4ac29-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ac29-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ac29-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ac29-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ac29-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4ac29-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac29-108">Parameters</span></span>

  - <span data-ttu-id="4ac29-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4ac29-109">lhs</span></span>  
    <span data-ttu-id="4ac29-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ac29-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4ac29-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="4ac29-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ac29-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4ac29-112">rhs</span></span>  
    <span data-ttu-id="4ac29-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ac29-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4ac29-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="4ac29-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4ac29-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ac29-115">Return value</span></span>

<span data-ttu-id="4ac29-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4ac29-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4ac29-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="4ac29-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ac29-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ac29-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ac29-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="4ac29-119">Reference</span></span>

[<span data-ttu-id="4ac29-120">JET_COLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="4ac29-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="4ac29-121">Mitglieder JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="4ac29-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="4ac29-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ac29-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
