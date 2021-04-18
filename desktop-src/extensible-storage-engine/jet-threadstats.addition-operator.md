---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Additions Operator'
title: JET_THREADSTATS. Additions Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351156"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="9ef89-103">JET_THREADSTATS. Additions Operator</span><span class="sxs-lookup"><span data-stu-id="9ef89-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="9ef89-104">Fügen Sie die Statistiken in zwei JET_THREADSTATS Strukturen hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ef89-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="9ef89-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ef89-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9ef89-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ef89-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef89-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef89-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="9ef89-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef89-108">Parameters</span></span>

  - <span data-ttu-id="9ef89-109">t1</span><span class="sxs-lookup"><span data-stu-id="9ef89-109">t1</span></span>  
    <span data-ttu-id="9ef89-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9ef89-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="9ef89-111">Der erste JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="9ef89-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ef89-112">T2</span><span class="sxs-lookup"><span data-stu-id="9ef89-112">t2</span></span>  
    <span data-ttu-id="9ef89-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9ef89-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="9ef89-114">Der zweite JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="9ef89-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9ef89-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ef89-115">Return value</span></span>

<span data-ttu-id="9ef89-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9ef89-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="9ef89-117">Eine JET_THREADSTATS, die das Ergebnis der Hinzufügung der Statistiken in T1 und T2 enthält.</span><span class="sxs-lookup"><span data-stu-id="9ef89-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ef89-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ef89-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ef89-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="9ef89-119">Reference</span></span>

[<span data-ttu-id="9ef89-120">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="9ef89-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="9ef89-121">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="9ef89-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="9ef89-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="9ef89-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
