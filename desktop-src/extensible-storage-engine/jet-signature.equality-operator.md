---
description: 'Weitere Informationen finden Sie hier: JET_SIGNATURE. Gleichheits Operator'
title: JET_SIGNATURE. Gleichheits Operator
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752465"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="7e891-103">JET_SIGNATURE. Gleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="7e891-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="7e891-104">Bestimmt, ob zwei angegebene Instanzen von JET_SIGNATURE gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7e891-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="7e891-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e891-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e891-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e891-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e891-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e891-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7e891-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e891-108">Parameters</span></span>

  - <span data-ttu-id="7e891-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7e891-109">lhs</span></span>  
    <span data-ttu-id="7e891-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7e891-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="7e891-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e891-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e891-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7e891-112">rhs</span></span>  
    <span data-ttu-id="7e891-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="7e891-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="7e891-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="7e891-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e891-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e891-115">Return value</span></span>

<span data-ttu-id="7e891-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7e891-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7e891-117">True, wenn die beiden Instanzen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="7e891-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e891-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e891-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e891-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="7e891-119">Reference</span></span>

[<span data-ttu-id="7e891-120">JET_SIGNATURE Struktur</span><span class="sxs-lookup"><span data-stu-id="7e891-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="7e891-121">Mitglieder JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7e891-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="7e891-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7e891-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
