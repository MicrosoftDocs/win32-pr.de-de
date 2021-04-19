---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Subtract-Methode'
title: JET_THREADSTATS. Subtract-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366101"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="40c67-103">JET_THREADSTATS. Subtract-Methode</span><span class="sxs-lookup"><span data-stu-id="40c67-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="40c67-104">Berechnen Sie den Unterschied in den Statistiken zwischen zwei JET_THREADSTATS Strukturen.</span><span class="sxs-lookup"><span data-stu-id="40c67-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="40c67-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40c67-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="40c67-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40c67-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40c67-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40c67-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="40c67-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="40c67-108">Parameters</span></span>

  - <span data-ttu-id="40c67-109">t1</span><span class="sxs-lookup"><span data-stu-id="40c67-109">t1</span></span>  
    <span data-ttu-id="40c67-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="40c67-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="40c67-111">Der erste JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="40c67-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="40c67-112">T2</span><span class="sxs-lookup"><span data-stu-id="40c67-112">t2</span></span>  
    <span data-ttu-id="40c67-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="40c67-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="40c67-114">Der zweite JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="40c67-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="40c67-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40c67-115">Return value</span></span>

<span data-ttu-id="40c67-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="40c67-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="40c67-117">Eine JET_THREADSTATS, die den Unterschied in den Statistiken zwischen T1 und T2 enthält.</span><span class="sxs-lookup"><span data-stu-id="40c67-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40c67-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40c67-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40c67-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="40c67-119">Reference</span></span>

[<span data-ttu-id="40c67-120">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="40c67-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="40c67-121">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="40c67-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="40c67-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="40c67-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
