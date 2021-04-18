---
description: 'Weitere Informationen finden Sie hier: JET_DBID. Ungleichheits Operator'
title: JET_DBID. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10dc41be66e687f7cba277dcbd7486e08ae2ad74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345098"
---
# <a name="jet_dbidinequality-operator"></a><span data-ttu-id="34d48-103">JET_DBID. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="34d48-103">JET_DBID.Inequality operator</span></span>

<span data-ttu-id="34d48-104">Bestimmt, ob zwei angegebene Instanzen von JET_DBID nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="34d48-104">Determines whether two specified instances of JET_DBID are not equal.</span></span>

<span data-ttu-id="34d48-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34d48-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34d48-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34d48-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34d48-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d48-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="34d48-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d48-108">Parameters</span></span>

  - <span data-ttu-id="34d48-109">LHS</span><span class="sxs-lookup"><span data-stu-id="34d48-109">lhs</span></span>  
    <span data-ttu-id="34d48-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="34d48-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="34d48-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="34d48-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="34d48-112">rhs</span><span class="sxs-lookup"><span data-stu-id="34d48-112">rhs</span></span>  
    <span data-ttu-id="34d48-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="34d48-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="34d48-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="34d48-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="34d48-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34d48-115">Return value</span></span>

<span data-ttu-id="34d48-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="34d48-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="34d48-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="34d48-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34d48-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34d48-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34d48-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="34d48-119">Reference</span></span>

[<span data-ttu-id="34d48-120">JET_DBID Struktur</span><span class="sxs-lookup"><span data-stu-id="34d48-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="34d48-121">Mitglieder JET_DBID</span><span class="sxs-lookup"><span data-stu-id="34d48-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="34d48-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="34d48-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
