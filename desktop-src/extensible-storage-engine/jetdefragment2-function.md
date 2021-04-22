---
description: 'Weitere Informationen zu: JetDefragment2-Funktion'
title: JetDefragment2-Funktion
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838804"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="bbbe8-103">JetDefragment2-Funktion</span><span class="sxs-lookup"><span data-stu-id="bbbe8-103">JetDefragment2 Function</span></span>


<span data-ttu-id="bbbe8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bbbe8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="bbbe8-105">JetDefragment2-Funktion</span><span class="sxs-lookup"><span data-stu-id="bbbe8-105">JetDefragment2 Function</span></span>

<span data-ttu-id="bbbe8-106">Die **JetDefragment2-Funktion** startet und beendet Datenbankdefragmentierungsaufgaben, wodurch die Datenorganisation innerhalb einer Datenbank verbessert wird, wobei ein Rückrufparameter verfügbar ist, um den Fortschritt der Defragmentierung zu melden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="bbbe8-107">Dies wird durchgeführt, um das Wachstum der Datenbank zu begrenzen, indem die vorhandene Datenträgerzuordnung innerhalb der Datenbank effizienter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="bbbe8-108">Sie kann auch den Arbeitssatz reduzieren, indem sichergestellt wird, dass die Daten genauer gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="bbbe8-109">Schließlich kann sie die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="bbbe8-110">**Windows XP:**  **JetDefragment2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="bbbe8-111">**JetDefragment2** enthält auch einen Rückruffunktionsparameter, der zum Melden des Fortschritts des Defragmentierungsprozesses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="bbbe8-112">Die Datenbankdefragmentierung ist ein Onlinevorgang und unterbricht keine regulären Datenbankaktivitäten wie Abfragevorgänge oder Datenaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="bbbe8-113">**JetDefragment2** erstellt auch keine Kopie aller vorhandenen Daten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="bbbe8-114">Stattdessen wird eine Datenbank an Ort und Stelle defragmentiert.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="bbbe8-115">Schließlich stellt **JetDefragment2** den internen Datenbankspeicherplatz für die Wiederverwendung wieder her, gibt jedoch keinen zusätzlichen Speicherplatz für das Betriebssystemdateisystem frei.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="bbbe8-116">Das resultierende Format der Daten kann viel effizienter sein, ist aber im Allgemeinen nicht optimal.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="bbbe8-117">Die Defragmentierung ist auf die Freigabe von Datenbankseiten zur erneuten Verwendung beschränkt, die Daten enthalten, die bereits logisch gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="bbbe8-118">Durch die Defragmentierung können Datenbankseiten in einigen Fällen auch wiederverwendet werden, indem Daten von zwei Seiten kombiniert werden, wenn sie auf eine einzelne Seite passen.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="bbbe8-119">Dieser Vorgang unterscheidet sich von [JetCompact,](./jetcompact-function.md) bei dem eine Kopie einer schreibgeschützten Datenbank in eine äußerst optimale Form umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="bbbe8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbbe8-120">Parameters</span></span>

<span data-ttu-id="bbbe8-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-121">*sesid*</span></span>

<span data-ttu-id="bbbe8-122">Die Sitzung, die für diesen Aufruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-122">The session to use for this call.</span></span>

<span data-ttu-id="bbbe8-123">*Dbid*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-123">*dbid*</span></span>

<span data-ttu-id="bbbe8-124">Die zu defragmentierende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-124">The database to defragment.</span></span>

<span data-ttu-id="bbbe8-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-125">*szTableName*</span></span>

<span data-ttu-id="bbbe8-126">Manchmal *ist szTableName* erforderlich, und manchmal ist es verboten:</span><span class="sxs-lookup"><span data-stu-id="bbbe8-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="bbbe8-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-127">*grbit*</span></span> | <span data-ttu-id="bbbe8-128">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="bbbe8-129">Muss `NULL`lauten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="bbbe8-130">Gibt den Namen der tabelle/BTree an, die defragmentiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="bbbe8-131">*Andere*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-131">*other*</span></span> | <span data-ttu-id="bbbe8-132">Muss `NULL`lauten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="bbbe8-133">Die Defragmentierung wird für die gesamte Datenbank durchgeführt, die von der angegebenen Datenbank-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="bbbe8-134">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-134">*pcPasses*</span></span>

<span data-ttu-id="bbbe8-135">Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Anzahl von Defragmentierungsüberläufen fest.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="bbbe8-136">Beim Beenden eines Onlinedefragmentierungs-Task wird dieser optionale Ausgabepuffer auf die Anzahl der ausgeführten Durchläufe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="bbbe8-137">Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Onlinedefragmentierungsüberläufe unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="bbbe8-138">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-138">*pcSeconds*</span></span>

<span data-ttu-id="bbbe8-139">Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser optionale Eingabeparameter die maximale Zeit für die Defragmentierung fest.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="bbbe8-140">Beim Beenden eines Onlinedefragmentierungs-Task wird dieser optionale Ausgabepuffer auf die Dauer festgelegt, die für die Defragmentierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="bbbe8-141">Wenn dieser Parameter auf NULL festgelegt ist oder *pcSeconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="bbbe8-142">*Rückruf*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-142">*callback*</span></span>

<span data-ttu-id="bbbe8-143">Rückruffunktion, die bei der Defragmentierung regelmäßig aufruft, um den Fortschritt zu melden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="bbbe8-144">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-144">*grbit*</span></span> | <span data-ttu-id="bbbe8-145">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="bbbe8-146">Muss `NULL`lauten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="bbbe8-147">Muss `NULL`lauten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="bbbe8-148">*Andere*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-148">*other*</span></span> | <span data-ttu-id="bbbe8-149">Optional.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-149">Optional.</span></span>


<span data-ttu-id="bbbe8-150">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bbbe8-150">*grbit*</span></span>

<span data-ttu-id="bbbe8-151">Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbe8-152">Wert</span><span class="sxs-lookup"><span data-stu-id="bbbe8-152">Value</span></span></p></th>
<th><p><span data-ttu-id="bbbe8-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bbbe8-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="bbbe8-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-155">Diese Option wird verwendet, um den verfügbaren Speicherplatzteil der ESE-Datenbankspeicherplatzbelegung zu defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="bbbe8-156">Der Datenbankspeicherplatz ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="bbbe8-157">Der eigene Speicherplatz wird einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="bbbe8-158">Der verfügbare Speicherplatz ist im Verhalten viel dynamischer und erfordert eine größere Onlinedefragmentierung als speicherplatz- oder tabellen- oder indexeigene Daten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="bbbe8-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-160">Diese Option wird verwendet, um eine neue Defragmentierungsaufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="bbbe8-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-162">Diese Option wird verwendet, um eine vorhandene gestartete Defragmentierungsaufgabe zu beenden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="bbbe8-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-164">Diese Option wird verwendet, um eine durch szTableName angegebene B-Struktur zu defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="bbbe8-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-166">Diese Option wird verwendet, um OLD2 für die gesamte Datenbank aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bbbe8-167">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbbe8-167">Return Value</span></span>

<span data-ttu-id="bbbe8-168">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bbbe8-169">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bbbe8-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbe8-170">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bbbe8-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="bbbe8-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbbe8-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bbbe8-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-173">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bbbe8-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-175">Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></span><span class="sxs-lookup"><span data-stu-id="bbbe8-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="bbbe8-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-177">Die für die Defragmentierung ausgewählte Datenbank ist schreibgeschützt und kann nicht aktualisiert werden, einschließlich defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="bbbe8-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-179">Die gegebene Sitzung befindet sich im Zustand "Commit vorbereitet" und kann keine neuen Updates starten, bis für die aktuelle Transaktion ein Commit oder Rollback ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bbbe8-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-181">Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bbbe8-182">Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="bbbe8-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-184">Die gegebene Datenbank-ID passt nicht zu einer bekannten Datenbank in der -Instanz.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bbbe8-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-186">Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bbbe8-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-188">Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bbbe8-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-190">Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="bbbe8-191">Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bbbe8-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-193">Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="bbbe8-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-195">Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bbbe8-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-197">Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeichers nicht ausreicht, um alle ausstehenden Updates zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="bbbe8-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-199">Die option JET_bitDefragmentBatchStart wurde übergeben, aber eine Defragmentierungsaufgabe führt bereits die Defragmentierung für die angegebene Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="bbbe8-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="bbbe8-201">Die option JET_bitDefragmentBatchStop wurde übergeben, aber derzeit wird keine Defragmentierungsaufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbbe8-202">Bei Erfolg wird die angeforderte Aktion ausgeführt, entweder eine Defragmentierungsaufgabe für bestimmte Daten mit angegebenen Optionen zu starten, oder die Aktion zum Beenden einer vorhandenen Defragmentierungsaufgabe wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="bbbe8-203">Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Onlinedefragmentierungsauftrags nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="bbbe8-204">Es treten keine weiteren Nebeneffekte auf.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bbbe8-205">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbbe8-205">Remarks</span></span>

<span data-ttu-id="bbbe8-206">Die Onlinedefragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="bbbe8-207">Der Standardwert des Systemparameters ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="bbbe8-208">Bei Verwendung von [JetSetSystemParameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Onlinedefragmentierung zu deaktivieren oder sie selektiv nur für Datenbankspeicherplatzstrukturen, nur Datenbanken, nur Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="bbbe8-209">Wenn die Systemeinstellung für die Onlinedefragmentierung auf eine veraltete Einstellung festgelegt ist, behandelt **JetDefragment2** die Einstellung als JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="bbbe8-210">Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="bbbe8-211">Die Aufgabe wird als Thread im Prozess ausgeführt, der ESE hostet.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="bbbe8-212">Die Zum Starten des Onlinedefragmentierungstasks verwendete Sitzung kann anschließend für Datenbankvorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da der Defragmentierungstask eine eigene Sitzung zuordnet.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="bbbe8-213">Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startsitzung des Tasks zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bbbe8-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbbe8-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-215"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-216">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-217"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-218">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-219"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-220">In Esent.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-221"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-222">Verwenden Sie ESENT.lib.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbe8-223"><strong>Dll</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-224">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbe8-225"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bbbe8-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bbbe8-226">Wird als <strong>JetDefragment2W</strong> (Unicode) und <strong>JetDefragment2A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="bbbe8-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bbbe8-227">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bbbe8-227">See Also</span></span>

[<span data-ttu-id="bbbe8-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bbbe8-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bbbe8-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bbbe8-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bbbe8-230">JetCompact</span><span class="sxs-lookup"><span data-stu-id="bbbe8-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="bbbe8-231">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="bbbe8-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="bbbe8-232">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bbbe8-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="bbbe8-233">JetStopService</span><span class="sxs-lookup"><span data-stu-id="bbbe8-233">JetStopService</span></span>](./jetstopservice-function.md)
