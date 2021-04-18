---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE. Subtraktions Operator'
title: JET_RECSIZE. Subtraktions Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39516016
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be60da4aeeab78794f087e9c7095a16dd39eb378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352440"
---
# <a name="jet_recsizesubtraction-operator"></a><span data-ttu-id="e826c-103">JET_RECSIZE. Subtraktions Operator</span><span class="sxs-lookup"><span data-stu-id="e826c-103">JET_RECSIZE.Subtraction operator</span></span>

<span data-ttu-id="e826c-104">Berechnen Sie den Unterschied in den Größen zwischen zwei JET_RECSIZE Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e826c-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="e826c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e826c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e826c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e826c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e826c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e826c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left - right)
```

``` csharp
public static JET_RECSIZE operator -(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="e826c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e826c-108">Parameters</span></span>

  - <span data-ttu-id="e826c-109">Linker Join</span><span class="sxs-lookup"><span data-stu-id="e826c-109">left</span></span>  
    <span data-ttu-id="e826c-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e826c-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="e826c-111">Der erste JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e826c-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="e826c-112">Rechts</span><span class="sxs-lookup"><span data-stu-id="e826c-112">right</span></span>  
    <span data-ttu-id="e826c-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e826c-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="e826c-114">Der zweite JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e826c-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e826c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e826c-115">Return value</span></span>

<span data-ttu-id="e826c-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="e826c-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="e826c-117">Eine JET_RECSIZE, die den Unterschied in den Größen zwischen Links und rechts enthält.</span><span class="sxs-lookup"><span data-stu-id="e826c-117">A JET_RECSIZE containing the difference in sizes between left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e826c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e826c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e826c-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="e826c-119">Reference</span></span>

[<span data-ttu-id="e826c-120">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="e826c-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="e826c-121">Mitglieder JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e826c-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="e826c-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="e826c-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
