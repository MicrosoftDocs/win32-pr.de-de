---
description: Weitere Informationen finden Sie in der JET_RETINFO. itagsequence-Eigenschaft.
title: JET_RETINFO. itagsequence (Eigenschaft)
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218136"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="e7cfc-103">JET_RETINFO. itagsequence (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7cfc-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="e7cfc-104">Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="e7cfc-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="e7cfc-105">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="e7cfc-105">The array of values is one-based.</span></span> <span data-ttu-id="e7cfc-106">Der erste Wert ist Sequenz 1, nicht 0.</span><span class="sxs-lookup"><span data-stu-id="e7cfc-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="e7cfc-107">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e7cfc-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="e7cfc-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7cfc-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7cfc-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7cfc-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cfc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7cfc-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e7cfc-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7cfc-111">Property value</span></span>

<span data-ttu-id="e7cfc-112">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e7cfc-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e7cfc-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7cfc-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7cfc-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="e7cfc-114">Reference</span></span>

[<span data-ttu-id="e7cfc-115">JET_RETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="e7cfc-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="e7cfc-116">Mitglieder JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e7cfc-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="e7cfc-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e7cfc-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
