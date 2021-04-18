---
description: 'Weitere Informationen zu: Debug-Bit-Enumeration'
title: Debug-Enumeration
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350986"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="62700-103">Debug-Enumeration</span><span class="sxs-lookup"><span data-stu-id="62700-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="62700-104">Optionen für [jetdefragment (JET_SESID, JET_DBID, String, Int32, Int32, defraggrbit)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="62700-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="62700-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="62700-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="62700-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="62700-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="62700-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="62700-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="62700-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62700-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="62700-109">Member</span><span class="sxs-lookup"><span data-stu-id="62700-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="62700-110">Membername</span><span class="sxs-lookup"><span data-stu-id="62700-110">Member name</span></span></th>
<th><span data-ttu-id="62700-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62700-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="62700-112">Availspacetreesonly</span><span class="sxs-lookup"><span data-stu-id="62700-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="62700-113">Zerlegt den verfügbaren Platz Anteil der ESE-Daten Bank Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="62700-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="62700-114">Der Daten Bankbereich ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="62700-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="62700-115">Der Speicherplatz ist einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist.</span><span class="sxs-lookup"><span data-stu-id="62700-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="62700-116">Der verfügbare Speicherplatz ist weitaus dynamischer als das Verhalten und erfordert eine Inline Defragmentierung, die nicht dem Besitz des eigenen Speicherplatzes oder der Tabellen-oder Indexdaten entspricht.</span><span class="sxs-lookup"><span data-stu-id="62700-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="62700-117">Batchstart</span><span class="sxs-lookup"><span data-stu-id="62700-117">BatchStart</span></span></td>
<td><span data-ttu-id="62700-118">Startet eine neue defragmentierungsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="62700-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="62700-119">Batchstoppt</span><span class="sxs-lookup"><span data-stu-id="62700-119">BatchStop</span></span></td>
<td><span data-ttu-id="62700-120">Beendet eine defragmentierungsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="62700-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="62700-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62700-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62700-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="62700-122">Reference</span></span>

[<span data-ttu-id="62700-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="62700-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
