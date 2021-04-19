---
description: 'Weitere Informationen finden Sie hier: JET_SIGNATURE. Ungleichheits Operator'
title: JET_SIGNATURE. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646b97f37aea55ee3e9d1aa24e80b9d26ea82469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353841"
---
# <a name="jet_signatureinequality-operator"></a><span data-ttu-id="87464-103">JET_SIGNATURE. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="87464-103">JET_SIGNATURE.Inequality operator</span></span>

<span data-ttu-id="87464-104">Bestimmt, ob zwei angegebene Instanzen von JET_SIGNATURE nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="87464-104">Determines whether two specified instances of JET_SIGNATURE are not equal.</span></span>

<span data-ttu-id="87464-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87464-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87464-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="87464-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87464-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="87464-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="87464-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87464-108">Parameters</span></span>

  - <span data-ttu-id="87464-109">LHS</span><span class="sxs-lookup"><span data-stu-id="87464-109">lhs</span></span>  
    <span data-ttu-id="87464-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="87464-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="87464-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="87464-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="87464-112">rhs</span><span class="sxs-lookup"><span data-stu-id="87464-112">rhs</span></span>  
    <span data-ttu-id="87464-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="87464-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="87464-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="87464-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="87464-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87464-115">Return value</span></span>

<span data-ttu-id="87464-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="87464-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="87464-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="87464-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87464-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87464-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87464-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="87464-119">Reference</span></span>

[<span data-ttu-id="87464-120">JET_SIGNATURE Struktur</span><span class="sxs-lookup"><span data-stu-id="87464-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="87464-121">Mitglieder JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="87464-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="87464-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="87464-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
