---
description: 'Weitere Informationen über: jetdebug-Funktion'
title: Jetdebug-Funktion
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349938"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="72e45-103">Jetdebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="72e45-103">JetDefragment Function</span></span>


<span data-ttu-id="72e45-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="72e45-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="72e45-105">Jetdebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="72e45-105">JetDefragment Function</span></span>

<span data-ttu-id="72e45-106">Die **jetdefragment** -Funktion startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</span><span class="sxs-lookup"><span data-stu-id="72e45-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="72e45-107">Dies erfolgt, um das Daten Bank Wachstum einzuschränken, indem die vorhandene Datenträger Zuordnung effizienter in der Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="72e45-108">Außerdem kann der Arbeits Satz reduziert werden, indem sichergestellt wird, dass die Daten stärker verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="72e45-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="72e45-109">Schließlich kann die Anwendung die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="72e45-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="72e45-110">Die Daten Bank Defragmentierung ist ein Online Vorgang und unterbricht keine reguläre Datenbankaktivität, wie z. b. Abfrage Vorgänge oder Datenaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="72e45-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="72e45-111">**Jetdebug** enthält auch keine Kopie aller vorhandenen Daten.</span><span class="sxs-lookup"><span data-stu-id="72e45-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="72e45-112">Stattdessen wird eine Datenbank an Ort und Stelle zerlegt.</span><span class="sxs-lookup"><span data-stu-id="72e45-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="72e45-113">Schließlich stellt **jetdefragment** den internen Daten Bank Speicher für die erneute Verwendung wieder her, gibt jedoch keinen zusätzlichen Speicherplatz im Dateisystem des Betriebssystems frei.</span><span class="sxs-lookup"><span data-stu-id="72e45-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="72e45-114">Das resultierende Format der Daten kann viel effizienter sein, ist aber nicht in der Regel optimal.</span><span class="sxs-lookup"><span data-stu-id="72e45-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="72e45-115">Die Defragmentierung ist auf das Freigeben von Datenbankseiten zur erneuten Verwendung beschränkt, die bereits logisch gelöschte Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="72e45-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="72e45-116">Die Defragmentierung sorgt auch dafür, dass Datenbankseiten in einigen Fällen wieder verwendet werden können, indem Daten von zwei Seiten kombiniert werden, wenn Sie auf eine einzelne Seite passen.</span><span class="sxs-lookup"><span data-stu-id="72e45-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="72e45-117">Dieser Vorgang unterscheidet sich von [jetcompact](./jetcompact-function.md) , wodurch eine Kopie einer schreibgeschützten Datenbank in ein sehr optimales Formular umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="72e45-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e45-118">Parameters</span></span>

<span data-ttu-id="72e45-119">*-sid*</span><span class="sxs-lookup"><span data-stu-id="72e45-119">*sesid*</span></span>

<span data-ttu-id="72e45-120">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72e45-120">The session to use for this call.</span></span>

<span data-ttu-id="72e45-121">*DBID*</span><span class="sxs-lookup"><span data-stu-id="72e45-121">*dbid*</span></span>

<span data-ttu-id="72e45-122">Die Datenbank, die zerlegt wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-122">The database that will be defragmented.</span></span>

<span data-ttu-id="72e45-123">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="72e45-123">*szTableName*</span></span>

<span data-ttu-id="72e45-124">Nicht verwendeter Parameter.</span><span class="sxs-lookup"><span data-stu-id="72e45-124">Unused parameter.</span></span> <span data-ttu-id="72e45-125">Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="72e45-126">*pcpass*</span><span class="sxs-lookup"><span data-stu-id="72e45-126">*pcPasses*</span></span>

<span data-ttu-id="72e45-127">Wenn eine Online Defragmentierung gestartet wird, legt dieser Eingabeparameter die maximale Anzahl von Verläufen fest.</span><span class="sxs-lookup"><span data-stu-id="72e45-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="72e45-128">Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die Anzahl der durchgeführten Durchläufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e45-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="72e45-129">Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Online Defragmentierungs Überläufen unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="72e45-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="72e45-130">*pcseconds*</span><span class="sxs-lookup"><span data-stu-id="72e45-130">*pcSeconds*</span></span>

<span data-ttu-id="72e45-131">Beim Starten einer Online Defragmentierung-Aufgabe legt dieser Eingabeparameter die maximale Zeit für die Defragmentierung fest.</span><span class="sxs-lookup"><span data-stu-id="72e45-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="72e45-132">Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e45-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="72e45-133">Wenn dieser Parameter auf NULL festgelegt ist oder *pcseconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="72e45-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="72e45-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="72e45-134">*grbit*</span></span>

<span data-ttu-id="72e45-135">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="72e45-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72e45-136">Wert</span><span class="sxs-lookup"><span data-stu-id="72e45-136">Value</span></span></p></th>
<th><p><span data-ttu-id="72e45-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="72e45-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72e45-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="72e45-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="72e45-139">Zerlegt den verfügbaren Platz Anteil der ESE-Daten Bank Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="72e45-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="72e45-140">Der Daten Bankbereich ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="72e45-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="72e45-141">Der Speicherplatz ist einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist.</span><span class="sxs-lookup"><span data-stu-id="72e45-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="72e45-142">Der verfügbare Speicherplatz ist weitaus dynamischer als das Verhalten und erfordert eine Inline Defragmentierung, die nicht dem Besitz des eigenen Speicherplatzes oder der Tabellen-oder Indexdaten entspricht.</span><span class="sxs-lookup"><span data-stu-id="72e45-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="72e45-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="72e45-144">Startet eine neue defragmentierungsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="72e45-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="72e45-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="72e45-146">Beendet eine defragmentierungsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="72e45-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="72e45-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72e45-147">Return Value</span></span>

<span data-ttu-id="72e45-148">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="72e45-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="72e45-149">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="72e45-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72e45-150">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="72e45-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="72e45-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72e45-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72e45-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="72e45-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="72e45-153">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="72e45-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="72e45-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="72e45-155">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="72e45-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="72e45-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="72e45-157">Die für die Defragmentierung gewählte Datenbank ist schreibgeschützt und kann in keiner Weise aktualisiert werden, einschließlich der Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="72e45-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="72e45-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="72e45-159">Die angegebene Sitzung befindet sich im Status "vorbereitet für Commit" und kann erst dann neue Updates starten, wenn für die aktuelle Transaktion ein Commit oder ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="72e45-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="72e45-161">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="72e45-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="72e45-162">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72e45-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="72e45-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="72e45-164">Die angegebene Datenbank-ID stimmt nicht mit einer bekannten Datenbank in der Instanz von identisch.</span><span class="sxs-lookup"><span data-stu-id="72e45-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="72e45-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="72e45-166">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="72e45-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="72e45-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="72e45-168">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="72e45-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="72e45-170">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72e45-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="72e45-171">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72e45-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="72e45-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="72e45-173">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="72e45-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="72e45-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="72e45-175">Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="72e45-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="72e45-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="72e45-177">Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeicher nicht ausreicht, um alle ausstehenden Updates zu speichern.</span><span class="sxs-lookup"><span data-stu-id="72e45-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="72e45-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="72e45-179">Die JET_bitDefragmentBatchStart-Option wurde übergeben, aber eine defragmentierungsaufgabe führt bereits Defragmentierung für die angegebene Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="72e45-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="72e45-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="72e45-181">Die JET_bitDefragmentBatchStop-Option wurde erfolgreich ausgeführt, aber zurzeit wird keine defragmentierungsaufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e45-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72e45-182">Bei Erfolg wird die angeforderte Aktion zum Starten einer defragmentierungsaufgabe für eine bestimmte Daten mit den angegebenen Optionen ausgeführt, oder die Aktion zum Beenden einer vorhandenen defragmentierungsaufgabe wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e45-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="72e45-183">Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Online defragmentierungsauftrags nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e45-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="72e45-184">Es treten keine anderen Nebeneffekte auf.</span><span class="sxs-lookup"><span data-stu-id="72e45-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="72e45-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72e45-185">Remarks</span></span>

<span data-ttu-id="72e45-186">Die Online Defragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert.</span><span class="sxs-lookup"><span data-stu-id="72e45-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="72e45-187">Der Standardwert für den Systemparameter ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72e45-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="72e45-188">Mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Online Defragmentierung zu deaktivieren oder Sie selektiv nur für Daten Bank Raumstrukturen, nur Datenbanken, Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="72e45-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="72e45-189">Wenn die Systemeinstellung für die Online Defragmentierung auf eine veraltete Einstellung festgelegt ist, wird die Einstellung von **jetdefragment** als JET_OnlineDefragAll behandelt.</span><span class="sxs-lookup"><span data-stu-id="72e45-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="72e45-190">Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="72e45-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="72e45-191">Der Task wird in dem Prozess, der ESE gehostet, als Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e45-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="72e45-192">Die Sitzung, mit der die Online Defragmentierung-Aufgabe gestartet wird, kann anschließend für Daten Bank Vorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da die Defragmentierungs Aufgabe eine eigene Sitzung zuordnet.</span><span class="sxs-lookup"><span data-stu-id="72e45-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="72e45-193">Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startzeit der Aufgabe zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.</span><span class="sxs-lookup"><span data-stu-id="72e45-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="72e45-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72e45-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72e45-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-196">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="72e45-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-198">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="72e45-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-200">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="72e45-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-201"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-202">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="72e45-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72e45-203"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-204">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="72e45-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72e45-205"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="72e45-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="72e45-206">Implementiert als <strong>jetdebug</strong> (Unicode) und <strong>jetdebug</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="72e45-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="72e45-207">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72e45-207">See Also</span></span>

[<span data-ttu-id="72e45-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="72e45-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="72e45-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="72e45-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="72e45-210">Jetcompact</span><span class="sxs-lookup"><span data-stu-id="72e45-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="72e45-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="72e45-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="72e45-212">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="72e45-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="72e45-213">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="72e45-213">JetStopService</span></span>](./jetstopservice-function.md)
