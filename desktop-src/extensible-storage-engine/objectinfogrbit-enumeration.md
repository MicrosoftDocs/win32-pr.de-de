---
description: 'Weitere Informationen finden Sie hier: objectinfogrbit-Enumeration'
title: Objectinfogrbit-Enumeration
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349889"
---
# <a name="objectinfogrbit-enumeration"></a><span data-ttu-id="aa98e-103">Objectinfogrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="aa98e-103">ObjectInfoGrbit enumeration</span></span>

<span data-ttu-id="aa98e-104">Tabellen Optionen, die in [JET_OBJECTINFO](./jet-objectinfo-class.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa98e-104">Table options, used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="aa98e-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="aa98e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="aa98e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa98e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa98e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa98e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa98e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa98e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
```

## <a name="members"></a><span data-ttu-id="aa98e-109">Member</span><span class="sxs-lookup"><span data-stu-id="aa98e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="aa98e-110">Membername</span><span class="sxs-lookup"><span data-stu-id="aa98e-110">Member name</span></span></th>
<th><span data-ttu-id="aa98e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa98e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aa98e-112">Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="aa98e-112">Bookmark</span></span></td>
<td><span data-ttu-id="aa98e-113">Die Tabelle kann Lesezeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa98e-113">The table can have bookmarks.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="aa98e-114">Rollback</span><span class="sxs-lookup"><span data-stu-id="aa98e-114">Rollback</span></span></td>
<td><span data-ttu-id="aa98e-115">Für die Tabelle kann ein Rollback ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aa98e-115">The table can be rolled back.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aa98e-116">Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="aa98e-116">Updatable</span></span></td>
<td><span data-ttu-id="aa98e-117">Die Tabelle kann aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa98e-117">The table can be updated.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="aa98e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa98e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa98e-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="aa98e-119">Reference</span></span>

[<span data-ttu-id="aa98e-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa98e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
