---
description: Weitere Informationen finden Sie in der GOTO secondaryindexbookmarkgrbit-Enumeration.
title: GOTO secondaryindexbookmarkgrbit-Enumeration
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343387"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="e600a-103">GOTO secondaryindexbookmarkgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e600a-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="e600a-104">Optionen für [jetgoessecondaryindexbookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GOTO secondaryindexbookmarkgrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="e600a-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="e600a-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="e600a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e600a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e600a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e600a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e600a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e600a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e600a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="e600a-109">Member</span><span class="sxs-lookup"><span data-stu-id="e600a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e600a-110">Membername</span><span class="sxs-lookup"><span data-stu-id="e600a-110">Member name</span></span></th>
<th><span data-ttu-id="e600a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e600a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e600a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="e600a-112">None</span></span></td>
<td><span data-ttu-id="e600a-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="e600a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e600a-114">Bookmarkpermitvirtualcurrency</span><span class="sxs-lookup"><span data-stu-id="e600a-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="e600a-115">Wenn der Index Eintrag nicht mehr gefunden werden kann, wird der Cursor positioniert, wo der Index Eintrag bereits gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e600a-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="e600a-116">Der Vorgang schlägt weiterhin mit JET_errRecordDeleted fehl. Es ist jedoch möglich, zum nächsten oder vorherigen Index Eintrag relativ zum Index Eintrag zu wechseln, der jetzt fehlt.</span><span class="sxs-lookup"><span data-stu-id="e600a-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e600a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e600a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e600a-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="e600a-118">Reference</span></span>

[<span data-ttu-id="e600a-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e600a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
