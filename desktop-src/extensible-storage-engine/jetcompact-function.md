---
description: 'Weitere Informationen zu: jetcompact-Funktion'
title: Jetcompact-Funktion
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358946"
---
# <a name="jetcompact-function"></a><span data-ttu-id="22bdf-103">Jetcompact-Funktion</span><span class="sxs-lookup"><span data-stu-id="22bdf-103">JetCompact Function</span></span>


<span data-ttu-id="22bdf-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22bdf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="22bdf-105">Jetcompact-Funktion</span><span class="sxs-lookup"><span data-stu-id="22bdf-105">JetCompact Function</span></span>

<span data-ttu-id="22bdf-106">Die **jetcompact** -Funktion erstellt eine Kopie einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="22bdf-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="22bdf-107">Die Kopie wird zu einem für die Verwendung optimalen Zustand komprimiert.</span><span class="sxs-lookup"><span data-stu-id="22bdf-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="22bdf-108">Die Daten in den kopierten Daten werden entsprechend den Measures verpackt, die bei der Indexerstellung für die Indizes ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="22bdf-109">Auf diese Weise können komprimierte Daten so dicht wie möglich gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="22bdf-110">Alternativ können durch komprimierte Datenspeicher Platz für nachfolgende Daten Satz Vergrößerung oder Index Einfügungen reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="22bdf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="22bdf-111">Parameters</span></span>

<span data-ttu-id="22bdf-112">*-sid*</span><span class="sxs-lookup"><span data-stu-id="22bdf-112">*sesid*</span></span>

<span data-ttu-id="22bdf-113">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22bdf-113">The session to use for this call.</span></span>

<span data-ttu-id="22bdf-114">*szdatabasesrc*</span><span class="sxs-lookup"><span data-stu-id="22bdf-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="22bdf-115">Die Quelldatenbank, die komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-115">The source database that will be compacted.</span></span>

<span data-ttu-id="22bdf-116">*szdatabasedest*</span><span class="sxs-lookup"><span data-stu-id="22bdf-116">*szDatabaseDest*</span></span>

<span data-ttu-id="22bdf-117">Der Name, der für die komprimierte Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22bdf-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="22bdf-118">*pfnstatus*</span><span class="sxs-lookup"><span data-stu-id="22bdf-118">*pfnStatus*</span></span>

<span data-ttu-id="22bdf-119">Eine Rückruffunktion, die regelmäßig über den Daten Bank Compact-Vorgang aufgerufen werden kann, um den Status zu melden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="22bdf-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="22bdf-120">*pconvert*</span></span>

<span data-ttu-id="22bdf-121">Ein Zeiger, der verwendet wird, um eine Alternative ESE-DLL festzulegen, die zum Lesen der Quelldatenbank verwendet werden kann, und um optionale Parameter für einen **jetcompact** -Vorgang bereitzustellen, der eine Datenbank von einem früheren in ein späteres Versions Format umwandelt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="22bdf-122">Diese Funktion wurde in Windows Server 2003 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="22bdf-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="22bdf-123">*grbit*</span></span>

<span data-ttu-id="22bdf-124">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22bdf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="22bdf-125">Value</span></span></p></th>
<th><p><span data-ttu-id="22bdf-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22bdf-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="22bdf-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="22bdf-128">Wird verwendet, wenn die Quelldatenbank bekanntermaßen beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="22bdf-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="22bdf-129">Sie ermöglicht eine ganze Reihe neuer Verhalten, die so viele Daten wie möglich aus der Quelldatenbank retten sollen.</span><span class="sxs-lookup"><span data-stu-id="22bdf-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="22bdf-130"><strong>Jetcompact</strong> mit diesem Options Satz kann JET_errSuccess zurückgeben, aber nicht alle in der Quelldatenbank erstellten Daten kopieren.</span><span class="sxs-lookup"><span data-stu-id="22bdf-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="22bdf-131">Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</span><span class="sxs-lookup"><span data-stu-id="22bdf-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="22bdf-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="22bdf-133">Bewirkt, dass <strong>jetcompact</strong> Statistiken für die Quelldatenbank in einer Datei namens DFRGINFO.TXT abgibt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="22bdf-134">Die Statistik enthält den Namen der einzelnen Tabellen in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> , die groß genug sind, um getrennt vom Datensatz, die Anzahl der Blattseiten des gruppierten Indexes und die Anzahl der Blattseiten für lange Werte gespeichert zu werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="22bdf-135">Außerdem werden zusammenfassende Statistiken einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Daten Bank Komprimierung benötigten Zeit und des temporären Daten Bank Speicherplatzes ebenfalls ebenfalls gekippt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="22bdf-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22bdf-136">Return Value</span></span>

<span data-ttu-id="22bdf-137">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="22bdf-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="22bdf-138">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="22bdf-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22bdf-139">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22bdf-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="22bdf-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22bdf-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="22bdf-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="22bdf-142">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="22bdf-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="22bdf-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="22bdf-144">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="22bdf-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="22bdf-146">Ein <em>pconvert</em> -Zeiger ungleich NULL wurde angegeben, aber die verwendete Version von ESE unterstützt die Convert-Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="22bdf-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="22bdf-147">Diese Funktion wurde in der Windows Server 2003-Version von ESE entfernt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="22bdf-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="22bdf-149">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="22bdf-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="22bdf-150">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22bdf-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="22bdf-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="22bdf-152">Die Aufruf Sitzung befindet sich innerhalb einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="22bdf-152">The calling session is within a transaction.</span></span> <span data-ttu-id="22bdf-153"><strong>Jetcompact</strong> muss von einer Sitzung außerhalb einer Transaktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="22bdf-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="22bdf-155">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="22bdf-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="22bdf-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="22bdf-157">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="22bdf-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="22bdf-159">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="22bdf-160">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22bdf-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="22bdf-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="22bdf-162">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22bdf-163">Bei Erfolg wird die Quelldatenbank in die Zieldatenbank kopiert.</span><span class="sxs-lookup"><span data-stu-id="22bdf-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="22bdf-164">Die Zieldatenbank befindet sich in einem optimalen Zustand, z. b. befinden sich alle Tabellenindizes im angrenzenden logischen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="22bdf-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="22bdf-165">Jede Indexseite wird mit dem Betrag aufgefüllt, der beim ursprünglichen Erstellen der Indizes in der Quelldatenbank konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="22bdf-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="22bdf-166">Alle Daten-und metadateneinstellungen werden mit voller Treue kopiert, es sei denn, die REPAIR-Option wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="22bdf-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="22bdf-167">Wenn die REPAIR-Option angegeben wurde, wurden möglicherweise einige Daten aus der Quelldatenbank nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="22bdf-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="22bdf-168">Bei einem Fehler kann die Zieldatenbank vorhanden sein, ist aber keine vollständige Kopie der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="22bdf-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="22bdf-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22bdf-169">Remarks</span></span>

<span data-ttu-id="22bdf-170">Das Komprimieren einer Datenbank wird auch verwendet, um eine Datenbank von einem früheren Versions Format auf eine modernere Version zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22bdf-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="22bdf-171">Ein optionaler Parameter ist *pconvert*, der eine-Struktur enthält, die eine Beschreibung für eine frühere Version der dll enthalten kann, die zum Lesen des Quelldaten Bank Formats verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="22bdf-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="22bdf-172">Diese Funktion wurde in Windows Server 2003 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="22bdf-173">Im Anschluss an Windows Server 2003 können neue Versionen von ESE immer ältere Versionen des Daten Bank Formats lesen, sodass diese Funktion nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="22bdf-174">Die gewünschte Datendichte nach einem Compact-Vorgang wird beim Erstellen von Tabellen und Indizes angegeben.</span><span class="sxs-lookup"><span data-stu-id="22bdf-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="22bdf-175">Die Dichte muss zwischen 20% und 100% liegen.</span><span class="sxs-lookup"><span data-stu-id="22bdf-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="22bdf-176">Wenn eine Datenbank in erster Linie gelesen und nicht aktualisiert wird, wird die Dichte von Anwendungen auf 100% festgelegt, um die Anzahl der e/a-Vorgänge während der Abfrage Verarbeitung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="22bdf-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="22bdf-177">Wenn die Daten jedoch häufig mit Vorgängen aktualisiert werden, die die Größe der mit dem Datensatz gespeicherten Daten erhöhen, oder wenn häufig neue Daten eingefügt werden, wählt die Anwendung eine niedrigere Dichte aus, sodass Updates häufig benötigte Ressourcen finden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="22bdf-178">Der Vorgang der Komprimierung der Datenbank bewirkt, dass die Datenbank idealerweise entsprechend der von der Anwendung ausgewählten Füllung angelegt wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="22bdf-179">Die Daten Bank Komprimierung ist ein Offline Vorgang.</span><span class="sxs-lookup"><span data-stu-id="22bdf-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="22bdf-180">Sie kann nicht ausgeführt werden, während die Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22bdf-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="22bdf-181">Demzufolge erfolgt dies in der Regel im Rahmen eines Buildprozesses der Entwicklung einer Anwendung, die ein DataSet als Teil von sich selbst bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="22bdf-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="22bdf-182">Die Offline Daten Bank Komprimierung berührt jedes Bit von Daten in einer Datenbank und kann als Mittel zum Überprüfen der Konsistenz einer Datenbank verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="22bdf-183">Wenn eine Datenbank Fehler verdächtig ist, kann Sie komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="22bdf-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="22bdf-184">Wenn in der Komprimierung kein Fehler gefunden wird, ist bekannt, dass sich die Datenbank in einem gültigen Zustand für ESE befindet.</span><span class="sxs-lookup"><span data-stu-id="22bdf-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="22bdf-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22bdf-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-187">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="22bdf-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-189">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="22bdf-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-191">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="22bdf-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-192"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-193">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="22bdf-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22bdf-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-195">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="22bdf-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22bdf-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="22bdf-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="22bdf-197">Implementiert als <strong>jetcompactw</strong> (Unicode) und <strong>jetcompacta</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="22bdf-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="22bdf-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22bdf-198">See Also</span></span>

[<span data-ttu-id="22bdf-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="22bdf-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="22bdf-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="22bdf-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="22bdf-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="22bdf-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="22bdf-202">Jetdebug</span><span class="sxs-lookup"><span data-stu-id="22bdf-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="22bdf-203">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="22bdf-203">JetStopService</span></span>](./jetstopservice-function.md)
