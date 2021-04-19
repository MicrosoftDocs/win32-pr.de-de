---
description: 'Weitere Informationen finden Sie hier: JET_RECORDLIST. TableID-Eigenschaft'
title: JET_RECORDLIST. TableID-Eigenschaft
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.tableid(v=EXCHG.10)
ms:contentKeyID: 55103838
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.tableid
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_tableid
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9140bc662592f20c2c54606666ab76099326fd56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362623"
---
# <a name="jet_recordlisttableid-property"></a><span data-ttu-id="1dcfc-103">JET_RECORDLIST. TableID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1dcfc-103">JET_RECORDLIST.tableid property</span></span>

<span data-ttu-id="1dcfc-104">Ruft TableID der temporären Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="1dcfc-104">Gets tableid of the temporary table.</span></span> <span data-ttu-id="1dcfc-105">Dies sollte geschlossen werden, wenn die Tabelle nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1dcfc-105">This should be closed when the table is no longer needed.</span></span>

<span data-ttu-id="1dcfc-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1dcfc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1dcfc-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1dcfc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1dcfc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dcfc-108">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="1dcfc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1dcfc-109">Property value</span></span>

<span data-ttu-id="1dcfc-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dcfc-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1dcfc-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dcfc-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1dcfc-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="1dcfc-112">Reference</span></span>

[<span data-ttu-id="1dcfc-113">JET_RECORDLIST-Klasse</span><span class="sxs-lookup"><span data-stu-id="1dcfc-113">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="1dcfc-114">Mitglieder JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="1dcfc-114">JET_RECORDLIST members</span></span>](./jet-recordlist-members.md)

[<span data-ttu-id="1dcfc-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dcfc-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
