---
description: 'Weitere Informationen finden Sie hier: JET_HANDLE. Ungleichheits Operator'
title: JET_HANDLE. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5feee9739ad57103b71786ae7d1cdbf5f7e858ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348818"
---
# <a name="jet_handleinequality-operator"></a><span data-ttu-id="aa495-103">JET_HANDLE. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="aa495-103">JET_HANDLE.Inequality operator</span></span>

<span data-ttu-id="aa495-104">Bestimmt, ob zwei angegebene Instanzen von JET_HANDLE nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="aa495-104">Determines whether two specified instances of JET_HANDLE are not equal.</span></span>

<span data-ttu-id="aa495-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa495-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa495-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa495-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa495-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa495-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="aa495-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa495-108">Parameters</span></span>

  - <span data-ttu-id="aa495-109">LHS</span><span class="sxs-lookup"><span data-stu-id="aa495-109">lhs</span></span>  
    <span data-ttu-id="aa495-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aa495-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="aa495-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="aa495-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa495-112">rhs</span><span class="sxs-lookup"><span data-stu-id="aa495-112">rhs</span></span>  
    <span data-ttu-id="aa495-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aa495-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="aa495-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="aa495-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aa495-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa495-115">Return value</span></span>

<span data-ttu-id="aa495-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="aa495-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="aa495-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="aa495-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa495-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa495-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa495-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="aa495-119">Reference</span></span>

[<span data-ttu-id="aa495-120">JET_HANDLE Struktur</span><span class="sxs-lookup"><span data-stu-id="aa495-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="aa495-121">Mitglieder JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="aa495-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="aa495-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa495-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
