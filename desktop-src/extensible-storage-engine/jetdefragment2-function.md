---
description: 'Weitere Informationen finden Sie hier: JetDefragment2-Funktion'
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
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106360248"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="e0a81-103">JetDefragment2-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0a81-103">JetDefragment2 Function</span></span>


<span data-ttu-id="e0a81-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0a81-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="e0a81-105">JetDefragment2-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0a81-105">JetDefragment2 Function</span></span>

<span data-ttu-id="e0a81-106">Die **JetDefragment2** -Funktion startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern, wobei ein Rückruf Parameter verfügbar ist, um den Fortschritt der Defragmentierung zu melden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="e0a81-107">Dies erfolgt, um das Daten Bank Wachstum einzuschränken, indem die vorhandene Datenträger Zuordnung effizienter in der Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="e0a81-108">Außerdem kann der Arbeits Satz reduziert werden, indem sichergestellt wird, dass die Daten stärker verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="e0a81-109">Schließlich kann die Anwendung die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="e0a81-110">**Windows XP:**  **JetDefragment2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="e0a81-111">**JetDefragment2** enthält außerdem einen Rückruf Funktionsparameter, der verwendet wird, um einen Bericht über den Status des Defragmentierungsvorgangs zu berichten.</span><span class="sxs-lookup"><span data-stu-id="e0a81-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="e0a81-112">Die Daten Bank Defragmentierung ist ein Online Vorgang und unterbricht keine reguläre Datenbankaktivität, wie z. b. Abfrage Vorgänge oder Datenaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="e0a81-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="e0a81-113">**JetDefragment2** macht auch keine Kopie aller vorhandenen Daten.</span><span class="sxs-lookup"><span data-stu-id="e0a81-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="e0a81-114">Stattdessen wird eine Datenbank an Ort und Stelle zerlegt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="e0a81-115">Schließlich stellt **JetDefragment2** den internen Daten Bank Speicher für die erneute Verwendung wieder her, gibt jedoch keinen zusätzlichen Speicherplatz im Dateisystem des Betriebssystems frei.</span><span class="sxs-lookup"><span data-stu-id="e0a81-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="e0a81-116">Das resultierende Format der Daten kann viel effizienter sein, ist aber nicht in der Regel optimal.</span><span class="sxs-lookup"><span data-stu-id="e0a81-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="e0a81-117">Die Defragmentierung ist auf das Freigeben von Datenbankseiten zur erneuten Verwendung beschränkt, die bereits logisch gelöschte Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0a81-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="e0a81-118">Die Defragmentierung sorgt auch dafür, dass Datenbankseiten in einigen Fällen wieder verwendet werden können, indem Daten von zwei Seiten kombiniert werden, wenn Sie auf eine einzelne Seite passen.</span><span class="sxs-lookup"><span data-stu-id="e0a81-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="e0a81-119">Dieser Vorgang unterscheidet sich von [jetcompact](./jetcompact-function.md) , wodurch eine Kopie einer schreibgeschützten Datenbank in ein sehr optimales Formular umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="e0a81-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0a81-120">Parameters</span></span>

<span data-ttu-id="e0a81-121">*-sid*</span><span class="sxs-lookup"><span data-stu-id="e0a81-121">*sesid*</span></span>

<span data-ttu-id="e0a81-122">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0a81-122">The session to use for this call.</span></span>

<span data-ttu-id="e0a81-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e0a81-123">*dbid*</span></span>

<span data-ttu-id="e0a81-124">Die zu zerfragmentdatenbank.</span><span class="sxs-lookup"><span data-stu-id="e0a81-124">The database to defragment.</span></span>

<span data-ttu-id="e0a81-125">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="e0a81-125">*szTableName*</span></span>

<span data-ttu-id="e0a81-126">Nicht verwendeter Parameter.</span><span class="sxs-lookup"><span data-stu-id="e0a81-126">Unused parameter.</span></span> <span data-ttu-id="e0a81-127">Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="e0a81-128">*pcpass*</span><span class="sxs-lookup"><span data-stu-id="e0a81-128">*pcPasses*</span></span>

<span data-ttu-id="e0a81-129">Wenn eine Online Defragmentierung gestartet wird, wird durch diesen optionalen Eingabeparameter die maximale Anzahl von Defragmentierungs Läufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="e0a81-130">Wenn Sie eine Online Defragmentierung beenden, wird dieser optionale Ausgabepuffer auf die Anzahl der durchgeführten Durchgänge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="e0a81-131">Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Online Defragmentierungs Überläufen unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="e0a81-132">*pcseconds*</span><span class="sxs-lookup"><span data-stu-id="e0a81-132">*pcSeconds*</span></span>

<span data-ttu-id="e0a81-133">Beim Starten einer Online Defragmentierung-Aufgabe legt dieser optionale Eingabeparameter die maximale Zeit für die Defragmentierung fest.</span><span class="sxs-lookup"><span data-stu-id="e0a81-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="e0a81-134">Wenn Sie eine Online Defragmentierung beenden, wird dieser optionale Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="e0a81-135">Wenn dieser Parameter auf NULL festgelegt ist oder *pcseconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="e0a81-136">*Rückruf*</span><span class="sxs-lookup"><span data-stu-id="e0a81-136">*callback*</span></span>

<span data-ttu-id="e0a81-137">Rückruffunktion, die regelmäßig Aufrufe aufruft, um den Fortschritt zu melden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="e0a81-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e0a81-138">*grbit*</span></span>

<span data-ttu-id="e0a81-139">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0a81-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e0a81-140">Value</span></span></p></th>
<th><p><span data-ttu-id="e0a81-141">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0a81-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="e0a81-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="e0a81-143">Diese Option wird verwendet, um den verfügbaren Speicherplatz der ESE-Daten Bank Speicher Belegung zu defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="e0a81-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="e0a81-144">Der Daten Bankbereich ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="e0a81-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="e0a81-145">Der Speicherplatz ist einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist.</span><span class="sxs-lookup"><span data-stu-id="e0a81-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="e0a81-146">Der verfügbare Speicherplatz ist weitaus dynamischer als das Verhalten und erfordert eine Online Defragmentierung, die größer ist als der Speicherplatz im Besitz von Tabellen oder Indexdaten.</span><span class="sxs-lookup"><span data-stu-id="e0a81-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="e0a81-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="e0a81-148">Diese Option wird verwendet, um eine neue defragmentierungsaufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="e0a81-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="e0a81-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="e0a81-150">Diese Option wird verwendet, um eine vorhandene Defragmentierungs Aufgabe zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="e0a81-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="e0a81-152">Diese Option wird verwendet, um eine B-Struktur zu defragmentieren.</span><span class="sxs-lookup"><span data-stu-id="e0a81-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e0a81-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0a81-153">Return Value</span></span>

<span data-ttu-id="e0a81-154">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e0a81-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e0a81-155">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0a81-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0a81-156">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e0a81-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="e0a81-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0a81-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e0a81-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e0a81-159">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e0a81-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e0a81-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e0a81-161">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="e0a81-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e0a81-163">Die für die Defragmentierung gewählte Datenbank ist schreibgeschützt und kann in keiner Weise aktualisiert werden, einschließlich der Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="e0a81-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="e0a81-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="e0a81-165">Die angegebene Sitzung befindet sich im Status "vorbereitet für Commit" und kann erst dann neue Updates starten, wenn für die aktuelle Transaktion ein Commit oder ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e0a81-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e0a81-167">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e0a81-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e0a81-168">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0a81-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e0a81-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="e0a81-170">Die angegebene Datenbank-ID stimmt nicht mit einer bekannten Datenbank in der Instanz von identisch.</span><span class="sxs-lookup"><span data-stu-id="e0a81-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e0a81-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e0a81-172">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e0a81-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e0a81-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0a81-174">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e0a81-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e0a81-176">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e0a81-177">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0a81-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e0a81-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0a81-179">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="e0a81-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e0a81-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e0a81-181">Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</span><span class="sxs-lookup"><span data-stu-id="e0a81-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="e0a81-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="e0a81-183">Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeicher nicht ausreicht, um alle ausstehenden Updates zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0a81-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="e0a81-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="e0a81-185">Die JET_bitDefragmentBatchStart-Option wurde übergeben, aber eine defragmentierungsaufgabe führt bereits Defragmentierung für die angegebene Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="e0a81-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="e0a81-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="e0a81-187">Die JET_bitDefragmentBatchStop-Option wurde erfolgreich ausgeführt, aber zurzeit wird keine defragmentierungsaufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0a81-188">Bei Erfolg wird die angeforderte Aktion zum Starten einer defragmentierungsaufgabe für eine bestimmte Daten mit den angegebenen Optionen ausgeführt, oder die Aktion zum Beenden einer vorhandenen defragmentierungsaufgabe wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="e0a81-189">Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Online defragmentierungsauftrags nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="e0a81-190">Es treten keine anderen Nebeneffekte auf.</span><span class="sxs-lookup"><span data-stu-id="e0a81-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e0a81-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0a81-191">Remarks</span></span>

<span data-ttu-id="e0a81-192">Die Online Defragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e0a81-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="e0a81-193">Der Standardwert für den Systemparameter ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e0a81-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="e0a81-194">Mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Online Defragmentierung zu deaktivieren oder Sie selektiv nur für Daten Bank Raumstrukturen, nur Datenbanken, Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e0a81-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="e0a81-195">Wenn die Systemeinstellung für die Online Defragmentierung auf eine veraltete Einstellung festgelegt ist, wird die Einstellung von **JetDefragment2** als JET_OnlineDefragAll behandelt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="e0a81-196">Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0a81-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="e0a81-197">Der Task wird in dem Prozess, der ESE gehostet, als Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0a81-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="e0a81-198">Die Sitzung, mit der die Online Defragmentierung-Aufgabe gestartet wird, kann anschließend für Daten Bank Vorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da die Defragmentierungs Aufgabe eine eigene Sitzung zuordnet.</span><span class="sxs-lookup"><span data-stu-id="e0a81-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="e0a81-199">Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startzeit der Aufgabe zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0a81-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0a81-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0a81-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-202">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0a81-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-204">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e0a81-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-206">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e0a81-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-207"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-208">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0a81-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0a81-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-210">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0a81-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0a81-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e0a81-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e0a81-212">Implementiert als <strong>JetDefragment2W</strong> (Unicode) und <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e0a81-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0a81-213">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0a81-213">See Also</span></span>

[<span data-ttu-id="e0a81-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0a81-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0a81-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e0a81-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e0a81-216">Jetcompact</span><span class="sxs-lookup"><span data-stu-id="e0a81-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="e0a81-217">Jetdebug</span><span class="sxs-lookup"><span data-stu-id="e0a81-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="e0a81-218">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="e0a81-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e0a81-219">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="e0a81-219">JetStopService</span></span>](./jetstopservice-function.md)
