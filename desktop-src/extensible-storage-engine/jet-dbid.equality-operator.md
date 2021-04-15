---
description: 'Weitere Informationen finden Sie hier: JET_DBID. Gleichheits Operator'
title: JET_DBID. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f9e99de78665d07e1e5a800f5520a39eb05e74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527446"
---
# <a name="jet_dbidequality-operator"></a><span data-ttu-id="5a2af-103">JET_DBID. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="5a2af-103">JET_DBID.Equality operator</span></span>

<span data-ttu-id="5a2af-104">Bestimmt, ob zwei angegebene Instanzen von JET_DBID gleich sind.</span><span class="sxs-lookup"><span data-stu-id="5a2af-104">Determines whether two specified instances of JET_DBID are equal.</span></span>

<span data-ttu-id="5a2af-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a2af-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a2af-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a2af-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a2af-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="5a2af-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a2af-108">Parameters</span></span>

  - <span data-ttu-id="5a2af-109">LHS</span><span class="sxs-lookup"><span data-stu-id="5a2af-109">lhs</span></span>  
    <span data-ttu-id="5a2af-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a2af-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5a2af-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="5a2af-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="5a2af-112">rhs</span><span class="sxs-lookup"><span data-stu-id="5a2af-112">rhs</span></span>  
    <span data-ttu-id="5a2af-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5a2af-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5a2af-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="5a2af-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5a2af-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a2af-115">Return value</span></span>

<span data-ttu-id="5a2af-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5a2af-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="5a2af-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="5a2af-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a2af-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a2af-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a2af-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="5a2af-119">Reference</span></span>

[<span data-ttu-id="5a2af-120">JET_DBID Struktur</span><span class="sxs-lookup"><span data-stu-id="5a2af-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="5a2af-121">Mitglieder JET_DBID</span><span class="sxs-lookup"><span data-stu-id="5a2af-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="5a2af-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a2af-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
