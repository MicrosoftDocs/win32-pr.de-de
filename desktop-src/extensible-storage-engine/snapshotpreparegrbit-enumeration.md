---
description: 'Weitere Informationen finden Sie hier: snapshotpreparegrbit-Enumeration'
title: Snapshotpreparegrbit-Enumeration
TOCTitle: SnapshotPrepareGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.snapshotpreparegrbit(v=EXCHG.10)
ms:contentKeyID: 39515688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32c11c609f78cc96862f9c2f15d93266f40ae941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343958"
---
# <a name="snapshotpreparegrbit-enumeration"></a><span data-ttu-id="af4e1-103">Snapshotpreparegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="af4e1-103">SnapshotPrepareGrbit enumeration</span></span>

<span data-ttu-id="af4e1-104">Optionen für [jedessnapshotprepare (JET_OSSNAPID, snapshotpreparegrbit)](./api.jetossnapshotprepare-method.md).</span><span class="sxs-lookup"><span data-stu-id="af4e1-104">Options for [JetOSSnapshotPrepare(JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span></span>

<span data-ttu-id="af4e1-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="af4e1-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="af4e1-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af4e1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af4e1-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af4e1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af4e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="af4e1-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotPrepareGrbit
'Usage
Dim instance As SnapshotPrepareGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotPrepareGrbit
```

## <a name="members"></a><span data-ttu-id="af4e1-109">Member</span><span class="sxs-lookup"><span data-stu-id="af4e1-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="af4e1-110">Membername</span><span class="sxs-lookup"><span data-stu-id="af4e1-110">Member name</span></span></th>
<th><span data-ttu-id="af4e1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af4e1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af4e1-112">Keine</span><span class="sxs-lookup"><span data-stu-id="af4e1-112">None</span></span></td>
<td><span data-ttu-id="af4e1-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="af4e1-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="af4e1-114">IncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="af4e1-114">IncrementalSnapshot</span></span></td>
<td><span data-ttu-id="af4e1-115">Es werden nur Protokolldateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="af4e1-115">Only logfiles will be taken.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="af4e1-116">Copysnapshot</span><span class="sxs-lookup"><span data-stu-id="af4e1-116">CopySnapshot</span></span></td>
<td><span data-ttu-id="af4e1-117">Eine Kopier Momentaufnahme (normal oder inkrementell) ohne Protokoll abkürzen.</span><span class="sxs-lookup"><span data-stu-id="af4e1-117">A copy snapshot (normal or incremental) with no log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="af4e1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af4e1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af4e1-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="af4e1-119">Reference</span></span>

[<span data-ttu-id="af4e1-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="af4e1-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
