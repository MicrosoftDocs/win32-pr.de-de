---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNDEF. cbmax-Eigenschaft'
title: JET_COLUMNDEF. cbmax (Eigenschaft)
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103491
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 486507dc046617ea6689fcf1c5eac4199cfeecd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348856"
---
# <a name="jet_columndefcbmax-property"></a><span data-ttu-id="e2185-103">JET_COLUMNDEF. cbmax (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e2185-103">JET_COLUMNDEF.cbMax property</span></span>

<span data-ttu-id="e2185-104">Ruft die maximale Länge der Spalte ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="e2185-104">Gets or sets the maximum length of the column.</span></span> <span data-ttu-id="e2185-105">Dies ist nur für Spalten vom Typ [Text](./jet-coltyp-enumeration.md), [LONGTEXT](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) und [LONGBINARY](./jet-coltyp-enumeration.md)von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="e2185-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="e2185-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2185-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2185-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2185-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2185-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2185-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e2185-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e2185-109">Property value</span></span>

<span data-ttu-id="e2185-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e2185-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2185-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2185-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2185-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2185-112">Reference</span></span>

[<span data-ttu-id="e2185-113">JET_COLUMNDEF-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2185-113">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="e2185-114">Mitglieder JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="e2185-114">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="e2185-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2185-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
