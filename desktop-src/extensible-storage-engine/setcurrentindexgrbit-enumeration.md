---
description: Weitere Informationen finden Sie in der setcurrentindexgrbit-Enumeration.
title: Setcurrentindexgrbit-Enumeration
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359885"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="22c29-103">Setcurrentindexgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="22c29-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="22c29-104">Optionen für [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, setcurrentindexgrbit)](./api.jetsetcurrentindex2-method.md) und [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, setcurrentindexgrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="22c29-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="22c29-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="22c29-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="22c29-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22c29-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22c29-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22c29-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22c29-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c29-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="22c29-109">Member</span><span class="sxs-lookup"><span data-stu-id="22c29-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="22c29-110">Membername</span><span class="sxs-lookup"><span data-stu-id="22c29-110">Member name</span></span></th>
<th><span data-ttu-id="22c29-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22c29-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="22c29-112">Keine</span><span class="sxs-lookup"><span data-stu-id="22c29-112">None</span></span></td>
<td><span data-ttu-id="22c29-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="22c29-113">Default options.</span></span> <span data-ttu-id="22c29-114">Dies entspricht dem Wert von "muvefirst".</span><span class="sxs-lookup"><span data-stu-id="22c29-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="22c29-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="22c29-115">MoveFirst</span></span></td>
<td><span data-ttu-id="22c29-116">Gibt an, dass der Cursor auf dem ersten Eintrag des angegebenen Indexes positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22c29-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="22c29-117">Wenn der aktuelle Index ausgewählt wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="22c29-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="22c29-118">Nomove</span><span class="sxs-lookup"><span data-stu-id="22c29-118">NoMove</span></span></td>
<td><span data-ttu-id="22c29-119">Gibt an, dass der Cursor auf dem Index Eintrag des neuen Indexes positioniert werden soll, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="22c29-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="22c29-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c29-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22c29-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="22c29-121">Reference</span></span>

[<span data-ttu-id="22c29-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="22c29-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
