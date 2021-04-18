---
description: 'Weitere Informationen finden Sie unter: deletecolumngrbit-Enumeration'
title: Deletecolumngrbit-Enumeration
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357410"
---
# <a name="deletecolumngrbit-enumeration"></a><span data-ttu-id="7617a-103">Deletecolumngrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7617a-103">DeleteColumnGrbit enumeration</span></span>

<span data-ttu-id="7617a-104">Optionen für [JetDeleteColumn2 (JET_SESID, JET_TABLEID, String, deletecolumngrbit)](./api.jetdeletecolumn2-method.md).</span><span class="sxs-lookup"><span data-stu-id="7617a-104">Options for [JetDeleteColumn2(JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span></span>

<span data-ttu-id="7617a-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="7617a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7617a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7617a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7617a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7617a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7617a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7617a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
```

## <a name="members"></a><span data-ttu-id="7617a-109">Member</span><span class="sxs-lookup"><span data-stu-id="7617a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7617a-110">Membername</span><span class="sxs-lookup"><span data-stu-id="7617a-110">Member name</span></span></th>
<th><span data-ttu-id="7617a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7617a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7617a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="7617a-112">None</span></span></td>
<td><span data-ttu-id="7617a-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="7617a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7617a-114">Ignoretemplatecolumschlag</span><span class="sxs-lookup"><span data-stu-id="7617a-114">IgnoreTemplateColumns</span></span></td>
<td><span data-ttu-id="7617a-115">Die API sollte nur versuchen, Spalten in der abgeleiteten Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7617a-115">The API should only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="7617a-116">Wenn eine Spalte mit diesem Namen in der Basistabelle vorhanden ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7617a-116">If a column of that name exists in the base table it will be ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7617a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7617a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7617a-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="7617a-118">Reference</span></span>

[<span data-ttu-id="7617a-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7617a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
