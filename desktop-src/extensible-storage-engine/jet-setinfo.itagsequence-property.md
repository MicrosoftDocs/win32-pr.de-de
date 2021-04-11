---
description: Weitere Informationen finden Sie in der JET_SETINFO. itagsequence-Eigenschaft.
title: JET_SETINFO. itagsequence (Eigenschaft)
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128641"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="3d7be-103">JET_SETINFO. itagsequence (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d7be-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="3d7be-104">Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3d7be-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="3d7be-105">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="3d7be-105">The array of values is one-based.</span></span> <span data-ttu-id="3d7be-106">Der erste Wert ist Sequenz 1, nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3d7be-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="3d7be-107">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="3d7be-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="3d7be-108">Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3d7be-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="3d7be-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d7be-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d7be-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d7be-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d7be-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d7be-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3d7be-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3d7be-112">Property value</span></span>

<span data-ttu-id="3d7be-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3d7be-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d7be-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d7be-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d7be-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="3d7be-115">Reference</span></span>

[<span data-ttu-id="3d7be-116">JET_SETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d7be-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="3d7be-117">Mitglieder JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="3d7be-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="3d7be-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d7be-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
