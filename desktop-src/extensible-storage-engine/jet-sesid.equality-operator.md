---
description: 'Weitere Informationen finden Sie hier: JET_SESID. Gleichheits Operator'
title: JET_SESID. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 19e0550452fb0053978cabcdb393222c814c85f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484491"
---
# <a name="jet_sesidequality-operator"></a><span data-ttu-id="7d0de-103">JET_SESID. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="7d0de-103">JET_SESID.Equality operator</span></span>

<span data-ttu-id="7d0de-104">Bestimmt, ob zwei angegebene Instanzen von JET_SESID gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7d0de-104">Determines whether two specified instances of JET_SESID are equal.</span></span>

<span data-ttu-id="7d0de-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d0de-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d0de-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d0de-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d0de-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7d0de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d0de-108">Parameters</span></span>

  - <span data-ttu-id="7d0de-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7d0de-109">lhs</span></span>  
    <span data-ttu-id="7d0de-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d0de-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7d0de-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d0de-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d0de-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7d0de-112">rhs</span></span>  
    <span data-ttu-id="7d0de-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7d0de-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7d0de-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d0de-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7d0de-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d0de-115">Return value</span></span>

<span data-ttu-id="7d0de-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7d0de-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7d0de-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7d0de-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d0de-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d0de-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d0de-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="7d0de-119">Reference</span></span>

[<span data-ttu-id="7d0de-120">JET_SESID Struktur</span><span class="sxs-lookup"><span data-stu-id="7d0de-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="7d0de-121">Mitglieder JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7d0de-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="7d0de-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d0de-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
