---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Subtraktions Operator'
title: JET_THREADSTATS. Subtraktions Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39512217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtraction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a41455f05b91a582a1d8aae824ca5b426628cf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214387"
---
# <a name="jet_threadstatssubtraction-operator"></a><span data-ttu-id="91fb9-103">JET_THREADSTATS. Subtraktions Operator</span><span class="sxs-lookup"><span data-stu-id="91fb9-103">JET_THREADSTATS.Subtraction operator</span></span>

<span data-ttu-id="91fb9-104">Berechnen Sie den Unterschied in den Statistiken zwischen zwei JET_THREADSTATS Strukturen.</span><span class="sxs-lookup"><span data-stu-id="91fb9-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="91fb9-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="91fb9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="91fb9-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="91fb9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="91fb9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91fb9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 - t2)
```

``` csharp
public static JET_THREADSTATS operator -(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="91fb9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91fb9-108">Parameters</span></span>

  - <span data-ttu-id="91fb9-109">t1</span><span class="sxs-lookup"><span data-stu-id="91fb9-109">t1</span></span>  
    <span data-ttu-id="91fb9-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="91fb9-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="91fb9-111">Der erste JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="91fb9-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="91fb9-112">T2</span><span class="sxs-lookup"><span data-stu-id="91fb9-112">t2</span></span>  
    <span data-ttu-id="91fb9-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="91fb9-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="91fb9-114">Der zweite JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="91fb9-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="91fb9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91fb9-115">Return value</span></span>

<span data-ttu-id="91fb9-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="91fb9-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="91fb9-117">Eine JET_THREADSTATS, die den Unterschied in den Statistiken zwischen T1 und T2 enthält.</span><span class="sxs-lookup"><span data-stu-id="91fb9-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91fb9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91fb9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91fb9-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="91fb9-119">Reference</span></span>

[<span data-ttu-id="91fb9-120">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="91fb9-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="91fb9-121">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="91fb9-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="91fb9-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="91fb9-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
