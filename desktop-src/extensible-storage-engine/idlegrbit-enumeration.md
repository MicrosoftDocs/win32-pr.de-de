---
description: 'Weitere Informationen finden Sie hier: idlegrbit-Enumeration'
title: Idlegrbit-Enumeration
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215056"
---
# <a name="idlegrbit-enumeration"></a><span data-ttu-id="f44fd-103">Idlegrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="f44fd-103">IdleGrbit enumeration</span></span>

<span data-ttu-id="f44fd-104">Optionen für [jetidle (JET_SESID, idlegrbit)](./api.jetidle-method.md).</span><span class="sxs-lookup"><span data-stu-id="f44fd-104">Options for [JetIdle(JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span></span>

<span data-ttu-id="f44fd-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="f44fd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f44fd-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f44fd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f44fd-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f44fd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f44fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f44fd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
```

## <a name="members"></a><span data-ttu-id="f44fd-109">Member</span><span class="sxs-lookup"><span data-stu-id="f44fd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f44fd-110">Membername</span><span class="sxs-lookup"><span data-stu-id="f44fd-110">Member name</span></span></th>
<th><span data-ttu-id="f44fd-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f44fd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f44fd-112">Keine</span><span class="sxs-lookup"><span data-stu-id="f44fd-112">None</span></span></td>
<td><span data-ttu-id="f44fd-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="f44fd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f44fd-114">Flushbuffers</span><span class="sxs-lookup"><span data-stu-id="f44fd-114">FlushBuffers</span></span></td>
<td><span data-ttu-id="f44fd-115">Löst die Bereinigung des Versionsspeicher aus.</span><span class="sxs-lookup"><span data-stu-id="f44fd-115">Triggers cleanup of the version store.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f44fd-116">Kompakt</span><span class="sxs-lookup"><span data-stu-id="f44fd-116">Compact</span></span></td>
<td><span data-ttu-id="f44fd-117">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f44fd-117">Reserved for future use.</span></span> <span data-ttu-id="f44fd-118">Wenn dieses Flag angegeben wird, gibt die API <a href="hh564840(v=exchg.10).md">invalidgrbit</a>zurück.</span><span class="sxs-lookup"><span data-stu-id="f44fd-118">If this flag is specified, the API will return <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f44fd-119">GetStatus</span><span class="sxs-lookup"><span data-stu-id="f44fd-119">GetStatus</span></span></td>
<td><span data-ttu-id="f44fd-120">Gibt <a href="hh557250(v=exchg.10).md">idlefull</a> zurück, wenn der Versionsspeicher größer als der Halbwert ist.</span><span class="sxs-lookup"><span data-stu-id="f44fd-120">Returns <a href="hh557250(v=exchg.10).md">IdleFull</a> if version store is more than half full.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f44fd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f44fd-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f44fd-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="f44fd-122">Reference</span></span>

[<span data-ttu-id="f44fd-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f44fd-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
