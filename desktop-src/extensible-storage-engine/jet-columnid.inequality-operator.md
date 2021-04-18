---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID. Ungleichheits Operator'
title: JET_COLUMNID. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516136
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6b0856a5c551be06dd7f4b55f8f144c0e509f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358983"
---
# <a name="jet_columnidinequality-operator"></a><span data-ttu-id="e02be-103">JET_COLUMNID. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="e02be-103">JET_COLUMNID.Inequality operator</span></span>

<span data-ttu-id="e02be-104">Bestimmt, ob zwei angegebene Instanzen von JET_COLUMNID nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e02be-104">Determines whether two specified instances of JET_COLUMNID are not equal.</span></span>

<span data-ttu-id="e02be-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e02be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e02be-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e02be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e02be-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e02be-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="e02be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e02be-108">Parameters</span></span>

  - <span data-ttu-id="e02be-109">LHS</span><span class="sxs-lookup"><span data-stu-id="e02be-109">lhs</span></span>  
    <span data-ttu-id="e02be-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e02be-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e02be-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="e02be-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="e02be-112">rhs</span><span class="sxs-lookup"><span data-stu-id="e02be-112">rhs</span></span>  
    <span data-ttu-id="e02be-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e02be-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e02be-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="e02be-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e02be-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e02be-115">Return value</span></span>

<span data-ttu-id="e02be-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e02be-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e02be-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e02be-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e02be-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e02be-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e02be-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e02be-119">Reference</span></span>

[<span data-ttu-id="e02be-120">JET_COLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="e02be-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="e02be-121">Mitglieder JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e02be-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="e02be-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e02be-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
