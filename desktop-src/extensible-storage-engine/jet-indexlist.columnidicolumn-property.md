---
description: Weitere Informationen finden Sie in der JET_INDEXLIST. columnidicolumn-Eigenschaft.
title: JET_INDEXLIST. columnidicolumn (Eigenschaft)
TOCTitle: 'columnidiColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidicolumn(v=EXCHG.10)
ms:contentKeyID: 55103664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidiColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2759c04b60c15d5786306ec536c7eddb89b02172
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352443"
---
# <a name="jet_indexlistcolumnidicolumn-property"></a><span data-ttu-id="9f420-103">JET_INDEXLIST. columnidicolumn (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9f420-103">JET_INDEXLIST.columnidiColumn property</span></span>

<span data-ttu-id="9f420-104">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Index von dieser Spalte im Index Schlüssel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9f420-104">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="9f420-105">Die Spalte ist vom Typ [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="9f420-105">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="9f420-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f420-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f420-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f420-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f420-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f420-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidiColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidiColumn
```

``` csharp
public JET_COLUMNID columnidiColumn { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="9f420-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9f420-109">Property value</span></span>

<span data-ttu-id="9f420-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f420-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f420-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f420-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f420-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="9f420-112">Reference</span></span>

[<span data-ttu-id="9f420-113">JET_INDEXLIST-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f420-113">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="9f420-114">Mitglieder JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="9f420-114">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="9f420-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f420-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
