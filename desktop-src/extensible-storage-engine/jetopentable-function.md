---
description: 'Weitere Informationen zu: jetopentable-Funktion'
title: JetOpenTable-Funktion
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749705"
---
# <a name="jetopentable-function"></a><span data-ttu-id="7e3c7-103">JetOpenTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e3c7-103">JetOpenTable Function</span></span>


<span data-ttu-id="7e3c7-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e3c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="7e3c7-105">JetOpenTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="7e3c7-105">JetOpenTable Function</span></span>

<span data-ttu-id="7e3c7-106">Die **jetopentable** -Funktion öffnet einen Cursor für eine zuvor erstellte Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="7e3c7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e3c7-107">Parameters</span></span>

<span data-ttu-id="7e3c7-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-108">*sesid*</span></span>

<span data-ttu-id="7e3c7-109">Der zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-109">The database session context to use.</span></span>

<span data-ttu-id="7e3c7-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-110">*dbid*</span></span>

<span data-ttu-id="7e3c7-111">Der Daten Bank Bezeichner, der zum Suchen der Tabelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="7e3c7-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-112">*szTableName*</span></span>

<span data-ttu-id="7e3c7-113">Der Name der zu öffnenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-113">The name of the table to open.</span></span>

<span data-ttu-id="7e3c7-114">*pvparameters*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-114">*pvParameters*</span></span>

<span data-ttu-id="7e3c7-115">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-115">Deprecated.</span></span> <span data-ttu-id="7e3c7-116">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-116">Set to **NULL**.</span></span>

<span data-ttu-id="7e3c7-117">*cbparameters*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-117">*cbParameters*</span></span>

<span data-ttu-id="7e3c7-118">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-118">Deprecated.</span></span> <span data-ttu-id="7e3c7-119">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-119">Set to 0 (zero).</span></span>

<span data-ttu-id="7e3c7-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-120">*grbit*</span></span>

<span data-ttu-id="7e3c7-121">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e3c7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7e3c7-122">Value</span></span></p></th>
<th><p><span data-ttu-id="7e3c7-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7e3c7-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="7e3c7-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-125">Die Tabelle kann nicht für den Lesezugriff durch eine andere Daten banksitzung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="7e3c7-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-127">Die Tabelle kann nicht für den Schreibzugriff durch eine andere Daten banksitzung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="7e3c7-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-129">Die Seiten für diese Tabelle werden nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="7e3c7-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-131">Ermöglicht DDL-Änderungen in Tabellen, die als fixedddl gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="7e3c7-132">Diese Option muss mit der Option JET_bitTableDenyRead verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="7e3c7-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-134">Gibt einen Hinweis an, dass sich die Tabelle wahrscheinlich nicht im Puffer Cache befindet, und dass das vorab lesen für die Leistung von Vorteil sein kann.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="7e3c7-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-136">Fordert den schreibgeschützten Zugriff auf die Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="7e3c7-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-138">Die Tabelle sollte sehr aggressiv vom Datenträger abgerufen werden, da die Anwendung Sie sequenziell scannt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="7e3c7-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-140">Fordert Schreibzugriff auf die Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e3c7-141">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="7e3c7-141">*ptableid*</span></span>

<span data-ttu-id="7e3c7-142">Bei Erfolg verweist auf den Bezeichner der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="7e3c7-143">Bei einem Fehler ist der Inhalt für *pTableID* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="7e3c7-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e3c7-144">Return Value</span></span>

<span data-ttu-id="7e3c7-145">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7e3c7-146">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7e3c7-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e3c7-147">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7e3c7-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="7e3c7-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e3c7-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7e3c7-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-150">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="7e3c7-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-152"><em>DBID</em> ist kein gültiger Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="7e3c7-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-154">Es wurde eine ungültige Kombination von <em>grbit</em> übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="7e3c7-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-156">Der in <em>sztablename</em> angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="7e3c7-157">Weitere Informationen zu gültigen Tabellennamen finden Sie unter dem Parameter " <em>sztablename</em> " in <a href="gg269210(v=exchg.10).md">jetkreatetable</a>.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="7e3c7-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-159">Es wurde versucht, eine Tabelle zu öffnen, die in der Datenbank nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="7e3c7-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-161">Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="7e3c7-162">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="7e3c7-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-164">Die Tabelle wird von einem anderen Daten Bank Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="7e3c7-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-166">Eine nicht schwerwiegende Warnung, die angibt, dass die Tabelle vom System verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="7e3c7-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-168">Die Tabelle wird durch einen anderen Daten Bank Vorgang gesperrt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="7e3c7-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="7e3c7-170">Es wurde versucht, zu viele eindeutige Tabellen gleichzeitig zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="7e3c7-171">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7e3c7-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e3c7-172">Remarks</span></span>

<span data-ttu-id="7e3c7-173">Tabellen, die mit **jetopentable** geöffnet werden, sollten normalerweise mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="7e3c7-174">Die Ausnahme von dieser Regel tritt auf, wenn **jetopentable** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7e3c7-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="7e3c7-175">Beim Rollback einer Transaktion wird die Tabelle automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="7e3c7-176">In diesem Fall ist es ein Fehler, die Tabelle mit [jetclosetable](./jetclosetable-function.md)zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="7e3c7-177">Es ist zulässig, Systemtabellen mit **jetopentable** (z. b. MSysObjects, msysunicodefixup) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="7e3c7-178">Das Schema der Systemtabellen kann sich ändern, sodass der Zugriff auf Systemtabellen nicht empfehlenswert ist.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="7e3c7-179">Die Anzahl der eindeutigen Tabellen, die gleichzeitig geöffnet werden können, wird direkt durch *JET_paramMaxOpenTables* beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="7e3c7-180">Wenn die Tabelle momentan geöffnet ist, wird ein neuer Cursor für die Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="7e3c7-181">Cursor Ressourcen werden mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit *JET_paramMaxCursors* konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="7e3c7-182">Siehe auch [jetdupcursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="7e3c7-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7e3c7-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e3c7-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-185">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-187">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-189">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-190"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-191">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e3c7-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-193">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7e3c7-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e3c7-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7e3c7-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7e3c7-195">Implementiert als <strong>jetopentablew</strong> (Unicode) und <strong>jetopentablea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7e3c7-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7e3c7-196">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7e3c7-196">See Also</span></span>

[<span data-ttu-id="7e3c7-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7e3c7-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7e3c7-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7e3c7-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7e3c7-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7e3c7-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7e3c7-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7e3c7-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7e3c7-201">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="7e3c7-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="7e3c7-202">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="7e3c7-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="7e3c7-203">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="7e3c7-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="7e3c7-204">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="7e3c7-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7e3c7-205">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="7e3c7-205">Resource Parameters</span></span>](./resource-parameters.md)
