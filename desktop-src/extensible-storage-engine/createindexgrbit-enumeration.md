---
description: Weitere Informationen finden Sie in der "kreateingedexgrbit"-Enumeration.
title: Aufzählung von "kreateingedexgrbit"
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352354"
---
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="92d41-103">Aufzählung von "kreateingedexgrbit"</span><span class="sxs-lookup"><span data-stu-id="92d41-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="92d41-104">Optionen für jetkreateingedex.</span><span class="sxs-lookup"><span data-stu-id="92d41-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="92d41-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="92d41-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="92d41-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92d41-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92d41-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92d41-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92d41-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="92d41-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a><span data-ttu-id="92d41-109">Member</span><span class="sxs-lookup"><span data-stu-id="92d41-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="92d41-110">Membername</span><span class="sxs-lookup"><span data-stu-id="92d41-110">Member name</span></span></th>
<th><span data-ttu-id="92d41-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92d41-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-112">Keine</span><span class="sxs-lookup"><span data-stu-id="92d41-112">None</span></span></td>
<td><span data-ttu-id="92d41-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="92d41-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="92d41-114">Indexunique</span><span class="sxs-lookup"><span data-stu-id="92d41-114">IndexUnique</span></span></td>
<td><span data-ttu-id="92d41-115">Doppelte Indexeinträge (Schlüssel) sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="92d41-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="92d41-116">Dies wird erzwungen, wenn jetupdate aufgerufen wird, nicht wenn jetsetcolumn aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92d41-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-117">Indexprimary</span><span class="sxs-lookup"><span data-stu-id="92d41-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="92d41-118">Der Index ist ein primärer Index (gruppierter Index).</span><span class="sxs-lookup"><span data-stu-id="92d41-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="92d41-119">Jede Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="92d41-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="92d41-120">Wenn kein primärer Index explizit für eine Tabelle definiert wird, erstellt die Datenbank-Engine ihren eigenen primären Index.</span><span class="sxs-lookup"><span data-stu-id="92d41-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="92d41-121">Indexdisallownull</span><span class="sxs-lookup"><span data-stu-id="92d41-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="92d41-122">Keine der Spalten, für die der Index erstellt wird, kann einen NULL-Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="92d41-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-123">Index-gnorumull</span><span class="sxs-lookup"><span data-stu-id="92d41-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="92d41-124">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn alle indizierten Spalten NULL sind.</span><span class="sxs-lookup"><span data-stu-id="92d41-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="92d41-125">Index gnoreanynull</span><span class="sxs-lookup"><span data-stu-id="92d41-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="92d41-126">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn eine der indizierten Spalten NULL ist.</span><span class="sxs-lookup"><span data-stu-id="92d41-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-127">Index gnorefirstnull</span><span class="sxs-lookup"><span data-stu-id="92d41-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="92d41-128">Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn die erste indizierte Spalte NULL ist.</span><span class="sxs-lookup"><span data-stu-id="92d41-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="92d41-129">Indexlazyflush</span><span class="sxs-lookup"><span data-stu-id="92d41-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="92d41-130">Gibt an, dass die Index Vorgänge verzögert protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="92d41-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="92d41-131">JET_bitIndexLazyFlush wirkt sich nicht auf die Faulheit von Datenaktualisierungen aus.</span><span class="sxs-lookup"><span data-stu-id="92d41-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="92d41-132">Wenn die Indizierungs Vorgänge durch die Beendigung des Prozesses unterbrochen werden, kann die Wiederherstellung der Datenbank weiterhin in einen konsistenten Zustand versetzt werden, aber der Index ist möglicherweise nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92d41-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-133">Indexempty</span><span class="sxs-lookup"><span data-stu-id="92d41-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="92d41-134">Versuchen Sie nicht, den Index zu erstellen, da alle Einträge zu NULL ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="92d41-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="92d41-135">bei der Übergabe JET_bitIndexEmpty muss auch grbit JET_bitIgnoreAnyNull angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="92d41-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="92d41-136">Dies ist eine Leistungsverbesserung.</span><span class="sxs-lookup"><span data-stu-id="92d41-136">This is a performance enhancement.</span></span> <span data-ttu-id="92d41-137">Wenn z. b. eine neue Spalte zu einer Tabelle hinzugefügt wird, dann wird ein Index für diese neu hinzugefügte Spalte erstellt, dann werden alle Datensätze in der Tabelle gescannt, auch wenn Sie niemals dem Index hinzugefügt würden.</span><span class="sxs-lookup"><span data-stu-id="92d41-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="92d41-138">Durch angeben JET_bitIndexEmpty wird die Überprüfung der Tabelle ausgelassen, was möglicherweise sehr lange dauern kann.</span><span class="sxs-lookup"><span data-stu-id="92d41-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="92d41-139">Indexunversionierung</span><span class="sxs-lookup"><span data-stu-id="92d41-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="92d41-140">Bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="92d41-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="92d41-141">Normalerweise kann eine Sitzung in einer Transaktion in keiner anderen Sitzung einen Index Erstellungs Vorgang sehen.</span><span class="sxs-lookup"><span data-stu-id="92d41-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="92d41-142">Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt, sodass die zweite Indexerstellung einfach fehlschlägt, anstatt potenziell viele unnötige Daten Bank Vorgänge zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="92d41-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="92d41-143">Die zweite Transaktion ist möglicherweise nicht in der Lage, den Index sofort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="92d41-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="92d41-144">Der Index Erstellungs Vorgang muss durchgeführt werden, bevor er verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="92d41-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="92d41-145">Die Sitzung darf sich zurzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="92d41-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="92d41-146">Indexsortnullshigh</span><span class="sxs-lookup"><span data-stu-id="92d41-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="92d41-147">Die Angabe dieses Flags bewirkt, dass NULL-Werte nach den Daten für alle Spalten im Index sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="92d41-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="92d41-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92d41-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92d41-149">Referenz</span><span class="sxs-lookup"><span data-stu-id="92d41-149">Reference</span></span>

[<span data-ttu-id="92d41-150">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="92d41-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
