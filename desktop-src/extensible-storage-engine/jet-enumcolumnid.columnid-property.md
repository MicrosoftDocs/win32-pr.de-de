---
description: Weitere Informationen finden Sie in der JET_ENUMCOLUMNID. ColumnID-Eigenschaft.
title: JET_ENUMCOLUMNID. ColumnID-Eigenschaft
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128216"
---
# <a name="jet_enumcolumnidcolumnid-property"></a><span data-ttu-id="f7476-103">JET_ENUMCOLUMNID. ColumnID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7476-103">JET_ENUMCOLUMNID.columnid property</span></span>

<span data-ttu-id="f7476-104">Ruft die aufzuzählenden Spalten-ID ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7476-104">Gets or sets the columnid ID to enumerate.</span></span>

<span data-ttu-id="f7476-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7476-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7476-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7476-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7476-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7476-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f7476-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f7476-108">Property value</span></span>

<span data-ttu-id="f7476-109">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7476-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="remarks"></a><span data-ttu-id="f7476-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7476-110">Remarks</span></span>

<span data-ttu-id="f7476-111">Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen und ein entsprechender Slot im Ausgabe Array von JET_ENUMCOLUMN Strukturen mit dem Spalten Status JET_wrnColumnSkipped generiert.</span><span class="sxs-lookup"><span data-stu-id="f7476-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of JET_ENUMCOLUMN structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7476-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7476-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7476-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="f7476-113">Reference</span></span>

[<span data-ttu-id="f7476-114">JET_ENUMCOLUMNID-Klasse</span><span class="sxs-lookup"><span data-stu-id="f7476-114">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="f7476-115">Mitglieder JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="f7476-115">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="f7476-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7476-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
