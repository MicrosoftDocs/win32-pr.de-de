---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE. Additions Operator'
title: JET_RECSIZE. Additions Operator (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c41fae92f6177bf0c39138ad33988a74c482e0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749825"
---
# <a name="jet_recsizeaddition-operator"></a><span data-ttu-id="ac1f5-103">JET_RECSIZE. Additions Operator</span><span class="sxs-lookup"><span data-stu-id="ac1f5-103">JET_RECSIZE.Addition operator</span></span>

<span data-ttu-id="ac1f5-104">Fügen Sie die Größen in zwei JET_RECSIZE Strukturen hinzu.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-104">Add the sizes in two JET_RECSIZE structures.</span></span>

<span data-ttu-id="ac1f5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac1f5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ac1f5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac1f5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac1f5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="ac1f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac1f5-108">Parameters</span></span>

  - <span data-ttu-id="ac1f5-109">Linker Join</span><span class="sxs-lookup"><span data-stu-id="ac1f5-109">left</span></span>  
    <span data-ttu-id="ac1f5-110">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ac1f5-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="ac1f5-111">Der erste JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac1f5-112">Rechts</span><span class="sxs-lookup"><span data-stu-id="ac1f5-112">right</span></span>  
    <span data-ttu-id="ac1f5-113">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ac1f5-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="ac1f5-114">Der zweite JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ac1f5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac1f5-115">Return value</span></span>

<span data-ttu-id="ac1f5-116">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ac1f5-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="ac1f5-117">Eine JET_RECSIZE, die das Ergebnis des Hinzufügens der Größen in der linken und rechten Ecke enthält.</span><span class="sxs-lookup"><span data-stu-id="ac1f5-117">A JET_RECSIZE containing the result of adding the sizes in left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac1f5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac1f5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac1f5-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="ac1f5-119">Reference</span></span>

[<span data-ttu-id="ac1f5-120">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="ac1f5-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="ac1f5-121">Mitglieder JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="ac1f5-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="ac1f5-122">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac1f5-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
