---
description: Weitere Informationen finden Sie in der JET_DBINFOMISC. bkinfodiffprev-Eigenschaft.
title: JET_DBINFOMISC. bkinfodiffprev-Eigenschaft
TOCTitle: 'bkinfoDiffPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfodiffprev(v=EXCHG.10)
ms:contentKeyID: 39513441
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoDiffPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoDiffPrev
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd152d1dffbc4cf956129dfd886186dda0b33084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343290"
---
# <a name="jet_dbinfomiscbkinfodiffprev-property"></a><span data-ttu-id="14698-103">JET_DBINFOMISC. bkinfodiffprev-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14698-103">JET_DBINFOMISC.bkinfoDiffPrev property</span></span>

<span data-ttu-id="14698-104">Ruft Informationen zur letzten erfolgreichen differenziellen Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="14698-104">Gets information about the last successful differential backup.</span></span> <span data-ttu-id="14698-105">Wird zurückgesetzt, wenn [bkinfofullprev](./jet-dbinfomisc.bkinfofullprev-property.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="14698-105">Reset when [bkinfoFullPrev](./jet-dbinfomisc.bkinfofullprev-property.md) is set.</span></span>

<span data-ttu-id="14698-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14698-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14698-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14698-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14698-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="14698-108">Syntax</span></span>

``` vb
'Declaration
Public Property bkinfoDiffPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoDiffPrev
```

``` csharp
public JET_BKINFO bkinfoDiffPrev { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="14698-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="14698-109">Property value</span></span>

<span data-ttu-id="14698-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="14698-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="14698-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14698-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14698-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="14698-112">Reference</span></span>

[<span data-ttu-id="14698-113">JET_DBINFOMISC-Klasse</span><span class="sxs-lookup"><span data-stu-id="14698-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="14698-114">Mitglieder JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="14698-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="14698-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="14698-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
