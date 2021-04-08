---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID. rgtagsequence-Eigenschaft'
title: JET_ENUMCOLUMNID. rgtagsequence (Eigenschaft)
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749857"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="05e7a-103">JET_ENUMCOLUMNID. rgtagsequence (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="05e7a-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="05e7a-104">Ruft das Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="05e7a-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="05e7a-105">Bei einem einzelnen Element handelt es sich um eine in JET_RETRIEVECOLUMN definierte itagsequence.</span><span class="sxs-lookup"><span data-stu-id="05e7a-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="05e7a-106">Eine itagsequence-Wert von 0 (null) bedeutet "Skip".</span><span class="sxs-lookup"><span data-stu-id="05e7a-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="05e7a-107">Eine itagsequence von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.</span><span class="sxs-lookup"><span data-stu-id="05e7a-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="05e7a-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05e7a-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05e7a-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="05e7a-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05e7a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e7a-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="05e7a-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05e7a-111">Property value</span></span>

<span data-ttu-id="05e7a-112">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="05e7a-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="05e7a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e7a-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05e7a-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="05e7a-114">Reference</span></span>

[<span data-ttu-id="05e7a-115">JET_ENUMCOLUMNID-Klasse</span><span class="sxs-lookup"><span data-stu-id="05e7a-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="05e7a-116">Mitglieder JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="05e7a-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="05e7a-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="05e7a-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
