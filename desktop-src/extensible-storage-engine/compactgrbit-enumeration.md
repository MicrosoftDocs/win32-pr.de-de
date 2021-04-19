---
description: 'Weitere Informationen finden Sie hier: compactgrbit-Enumeration'
title: Compactgrbit-Enumeration
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350505"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="06b14-103">Compactgrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="06b14-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="06b14-104">Optionen für [jetcompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, compactgrbit)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="06b14-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="06b14-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="06b14-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="06b14-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06b14-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06b14-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06b14-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06b14-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06b14-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
```

## <a name="members"></a><span data-ttu-id="06b14-109">Member</span><span class="sxs-lookup"><span data-stu-id="06b14-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="06b14-110">Membername</span><span class="sxs-lookup"><span data-stu-id="06b14-110">Member name</span></span></th>
<th><span data-ttu-id="06b14-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06b14-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="06b14-112">Keine</span><span class="sxs-lookup"><span data-stu-id="06b14-112">None</span></span></td>
<td><span data-ttu-id="06b14-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="06b14-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="06b14-114">Stats</span><span class="sxs-lookup"><span data-stu-id="06b14-114">Stats</span></span></td>
<td><span data-ttu-id="06b14-115">Bewirkt, dass jetcompact Statistiken für die Quelldatenbank in einer Datei namens DFRGINFO.TXT abgibt.</span><span class="sxs-lookup"><span data-stu-id="06b14-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="06b14-116">Die Statistik enthält den Namen der einzelnen Tabellen in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="hh577895(v=exchg.10).md">LONGTEXT</a> oder <a href="hh577895(v=exchg.10).md">LONGBINARY</a> , die groß genug sind, um getrennt vom Datensatz, die Anzahl der Blattseiten des gruppierten Indexes und die Anzahl der Blattseiten für lange Werte gespeichert zu werden.</span><span class="sxs-lookup"><span data-stu-id="06b14-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="06b14-117">Außerdem werden zusammenfassende Statistiken einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Daten Bank Komprimierung benötigten Zeit und des temporären Daten Bank Speicherplatzes ebenfalls ebenfalls gekippt.</span><span class="sxs-lookup"><span data-stu-id="06b14-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="06b14-118">Reparieren</span><span class="sxs-lookup"><span data-stu-id="06b14-118">Repair</span></span></td>
<td><span data-ttu-id="06b14-119"><strong>Veraltet.</strong></span><span class="sxs-lookup"><span data-stu-id="06b14-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="06b14-120">Wird verwendet, wenn die Quelldatenbank bekanntermaßen beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="06b14-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="06b14-121">Sie ermöglicht eine ganze Reihe neuer Verhalten, die so viele Daten wie möglich aus der Quelldatenbank retten sollen.</span><span class="sxs-lookup"><span data-stu-id="06b14-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="06b14-122">Jetcompact mit diesem Options Satz kann <a href="hh564840(v=exchg.10).md">Erfolg</a> zurückgeben, aber nicht alle in der Quelldatenbank erstellten Daten kopieren.</span><span class="sxs-lookup"><span data-stu-id="06b14-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="06b14-123">Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</span><span class="sxs-lookup"><span data-stu-id="06b14-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="06b14-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06b14-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06b14-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="06b14-125">Reference</span></span>

[<span data-ttu-id="06b14-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="06b14-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
