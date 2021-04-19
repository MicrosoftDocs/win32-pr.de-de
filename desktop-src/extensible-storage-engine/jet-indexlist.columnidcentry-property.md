---
description: Weitere Informationen finden Sie in der JET_INDEXLIST. columnidcentry-Eigenschaft.
title: JET_INDEXLIST. columnidcentry-Eigenschaft
TOCTitle: 'columnidcEntry property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcentry(v=EXCHG.10)
ms:contentKeyID: 55103597
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcEntry
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcEntry
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49f3a2a8c22a869cd70a40da72b3e2915caa638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349366"
---
# <a name="jet_indexlistcolumnidcentry-property"></a><span data-ttu-id="f3ec8-103">JET_INDEXLIST. columnidcentry-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3ec8-103">JET_INDEXLIST.columnidcEntry property</span></span>

<span data-ttu-id="f3ec8-104">Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f3ec8-104">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="f3ec8-105">Dieser Wert ist nicht aktuell und wird nur von "API. jetcomputestats" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f3ec8-105">This value is not current and is only is updated by "Api.JetComputeStats".</span></span> <span data-ttu-id="f3ec8-106">Die Spalte ist vom Typ [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f3ec8-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="f3ec8-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3ec8-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3ec8-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3ec8-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ec8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3ec8-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcEntry As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcEntry
```

``` csharp
public JET_COLUMNID columnidcEntry { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f3ec8-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3ec8-110">Property value</span></span>

<span data-ttu-id="f3ec8-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f3ec8-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3ec8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3ec8-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3ec8-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="f3ec8-113">Reference</span></span>

[<span data-ttu-id="f3ec8-114">JET_INDEXLIST-Klasse</span><span class="sxs-lookup"><span data-stu-id="f3ec8-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="f3ec8-115">Mitglieder JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="f3ec8-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="f3ec8-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f3ec8-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
