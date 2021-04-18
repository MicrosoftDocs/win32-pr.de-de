---
description: Weitere Informationen finden Sie in der JET_RETINFO. columnidnexttaging-Eigenschaft.
title: JET_RETINFO. columnidnexttaging (Eigenschaft)
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64114b1e998d47a2610e414304e7837ecbb17fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368907"
---
# <a name="jet_retinfocolumnidnexttagged-property"></a><span data-ttu-id="25c6a-103">JET_RETINFO. columnidnexttaging (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25c6a-103">JET_RETINFO.columnidNextTagged property</span></span>

<span data-ttu-id="25c6a-104">Ruft das ColumnID der abgerufenen Spalte mit mehreren Werten oder geringer Dichte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID an jetretrievecolbin übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="25c6a-104">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span>

<span data-ttu-id="25c6a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25c6a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25c6a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25c6a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25c6a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c6a-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RETINFO
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="25c6a-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="25c6a-108">Property value</span></span>

<span data-ttu-id="25c6a-109">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25c6a-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="25c6a-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25c6a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25c6a-111">Referenz</span><span class="sxs-lookup"><span data-stu-id="25c6a-111">Reference</span></span>

[<span data-ttu-id="25c6a-112">JET_RETINFO-Klasse</span><span class="sxs-lookup"><span data-stu-id="25c6a-112">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="25c6a-113">Mitglieder JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="25c6a-113">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="25c6a-114">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="25c6a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
