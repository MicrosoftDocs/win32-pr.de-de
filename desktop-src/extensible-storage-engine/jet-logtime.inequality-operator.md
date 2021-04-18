---
description: 'Weitere Informationen finden Sie hier: JET_LOGTIME. Ungleichheits Operator'
title: JET_LOGTIME. Ungleichheits Operator
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511232
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ba95b6306984fcee5749e4b97d969713541851f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351159"
---
# <a name="jet_logtimeinequality-operator"></a><span data-ttu-id="f12ba-103">JET_LOGTIME. Ungleichheits Operator</span><span class="sxs-lookup"><span data-stu-id="f12ba-103">JET_LOGTIME.Inequality operator</span></span>

<span data-ttu-id="f12ba-104">Bestimmt, ob zwei angegebene Instanzen von JET_LOGTIME nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f12ba-104">Determines whether two specified instances of JET_LOGTIME are not equal.</span></span>

<span data-ttu-id="f12ba-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f12ba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f12ba-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f12ba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f12ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f12ba-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f12ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f12ba-108">Parameters</span></span>

  - <span data-ttu-id="f12ba-109">LHS</span><span class="sxs-lookup"><span data-stu-id="f12ba-109">lhs</span></span>  
    <span data-ttu-id="f12ba-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f12ba-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f12ba-111">Die erste zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="f12ba-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f12ba-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f12ba-112">rhs</span></span>  
    <span data-ttu-id="f12ba-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f12ba-113">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f12ba-114">Die zweite zu vergleichende Instanz.</span><span class="sxs-lookup"><span data-stu-id="f12ba-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f12ba-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f12ba-115">Return value</span></span>

<span data-ttu-id="f12ba-116">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f12ba-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f12ba-117">True, wenn die beiden-Instanzen nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f12ba-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f12ba-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f12ba-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f12ba-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="f12ba-119">Reference</span></span>

[<span data-ttu-id="f12ba-120">JET_LOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="f12ba-120">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="f12ba-121">Mitglieder JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="f12ba-121">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="f12ba-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f12ba-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
