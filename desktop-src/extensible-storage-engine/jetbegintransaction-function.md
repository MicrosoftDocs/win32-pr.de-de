---
description: Weitere Informationen finden Sie in der jetbegintransaction-Funktion.
title: JetBeginTransaction-Funktion
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342668"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="a1434-103">JetBeginTransaction-Funktion</span><span class="sxs-lookup"><span data-stu-id="a1434-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="a1434-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1434-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="a1434-105">JetBeginTransaction-Funktion</span><span class="sxs-lookup"><span data-stu-id="a1434-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="a1434-106">Die **jetbegintransaction** -Funktion bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="a1434-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="a1434-107">Diese Funktion kann in einer einzelnen Sitzung mehrmals aufgerufen werden, um die Erstellung zusätzlicher Speicherpunkte zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="a1434-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="a1434-108">Diese Speicherpunkte können verwendet werden, um Änderungen am Status der Datenbank selektiv beizubehalten oder zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="a1434-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="a1434-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1434-109">Parameters</span></span>

<span data-ttu-id="a1434-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="a1434-110">*sesid*</span></span>

<span data-ttu-id="a1434-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1434-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="a1434-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1434-112">Return Value</span></span>

<span data-ttu-id="a1434-113">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a1434-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a1434-114">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a1434-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1434-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a1434-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="a1434-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1434-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1434-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a1434-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a1434-118">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a1434-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a1434-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a1434-120">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a1434-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1434-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a1434-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a1434-122">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a1434-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a1434-123">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1434-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a1434-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a1434-125">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1434-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1434-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a1434-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1434-127">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1434-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a1434-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a1434-129">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1434-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a1434-130">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1434-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1434-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a1434-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a1434-132">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a1434-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="a1434-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="a1434-134">Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkt Tiefe hat, die von der Datenbank-Engine zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a1434-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1434-135">Bei Erfolg wird die angegebene Sitzung innerhalb einer Transaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1434-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="a1434-136">Wenn sich die Sitzung zuvor in einer Transaktion befand, wird ein neuer Sicherungspunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="a1434-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="a1434-137">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="a1434-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="a1434-138">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="a1434-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a1434-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1434-139">Remarks</span></span>

<span data-ttu-id="a1434-140">Die Datenbank-Engine stellt ein Snapshot-Isolations Modell für Ihre Transaktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a1434-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="a1434-141">Dies bedeutet Folgendes: Wenn eine Sitzung zum ersten Mal in einen Transaktionszustand gelangt, wird die gesamte Datenbank in der Zeit zu Beginn der Transaktion fixiert.</span><span class="sxs-lookup"><span data-stu-id="a1434-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="a1434-142">Eine Sitzung muss keine Daten Sperren, da Sie stets auf die entsprechende Version dieser Daten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="a1434-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="a1434-143">Dies bedeutet, dass eine Sitzung, die Daten aktualisiert, niemals eine andere Sitzung daran hindern wird, diese Daten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="a1434-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="a1434-144">Eine weitere Konsequenz der Verwendung der Momentaufnahme Isolation ist das Sperr Modell, das für Updates verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1434-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="a1434-145">Die Datenbank-Engine gibt eine Schreibsperre für ein bestimmtes Datenelement an die erste Sitzung aus, die Sie anfordert.</span><span class="sxs-lookup"><span data-stu-id="a1434-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="a1434-146">Diese Schreibsperre wird aufgehoben, wenn die Transaktion entweder vollständig committet oder abgebrochen wurde, sodass die Sitzung nicht mehr in einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1434-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="a1434-147">Während eine Sitzung eine Schreibsperre enthält, wird jede andere Sitzung, die dieselbe Schreibsperre anfordert, nicht blockiert, bis die Schreibsperre verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a1434-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="a1434-148">Stattdessen schlägt diese zweite Sitzung sofort mit JET_errWriteConflict fehl.</span><span class="sxs-lookup"><span data-stu-id="a1434-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="a1434-149">Um diesen Konflikt zu lösen, muss die zweite Sitzung die Transaktion vollständig abbrechen (oder Committe). warten Sie einige Zeit, bis die erste Sitzung einen Commit oder Abbruch der Transaktion durchgeführt hat, und beginnen Sie dann erneut.</span><span class="sxs-lookup"><span data-stu-id="a1434-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="a1434-150">Zur Unterstützung der Momentaufnahmenisolation speichert die Datenbank-Engine alle Versionen aller geänderten Daten im Arbeitsspeicher, seit die älteste aktive Transaktion in einer Sitzung zum ersten Mal gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1434-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="a1434-151">Dies hat wichtige Auswirkungen auf Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a1434-151">This has important implications for your application.</span></span> <span data-ttu-id="a1434-152">Jedes Verhalten, das eine große Anzahl von Versionen im Arbeitsspeicher aufführt, kann dazu führen, dass die Instanz die maximale Versionsspeicher Größe abbaut (Weitere Informationen finden Sie unter [JET_paramMaxVerPages](./resource-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md) ).</span><span class="sxs-lookup"><span data-stu-id="a1434-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="a1434-153">Dieses Verhalten umfasst, ist aber nicht auf sehr große Updates in einer einzelnen Transaktion und sehr lang andauernden Transaktionen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a1434-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="a1434-154">Daher ist es sehr wichtig, die Versionsspeicher Größe für die erwartete Transaktions Last der Anwendung ordnungsgemäß zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a1434-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="a1434-155">Es ist auch wichtig, die Anzahl der Updates, die in einer einzelnen Transaktion ausgeführt werden, zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="a1434-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="a1434-156">Außerdem ist es wichtig, Transaktionen so kurz wie möglich in Szenarien mit hoher Auslastung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1434-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="a1434-157">Es wird dringend empfohlen, dass die Anwendung immer im Kontext einer Transaktion ist, wenn Sie ESE-APIs aufrufen, die Daten abrufen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a1434-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="a1434-158">Wenn dies nicht erfolgt, umschließt die Datenbank-Engine automatisch jeden ESE-API-Aufrufe dieses Typs in einer Transaktion für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a1434-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="a1434-159">Die Kosten für diese sehr kurzen Transaktionen können in einigen Fällen schnell addiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1434-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="a1434-160">Das Standardverhalten der Engine besteht darin, die Verwendung einer Sitzung von dem Zeitpunkt, an dem der erste Aufruf von **jetbegintransaction** erfolgt, auf denselben Thread einzuschränken, bis zu dem Zeitpunkt, zu dem der übereinstimmende Aufruf von [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md) erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a1434-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="a1434-161">Dieses Verhalten kann geändert werden, um diese Einschränkung zu entfernen, indem ein benutzerdefinierter Sitzungs Kontext mithilfe von [jetort](./jetsetsessioncontext-function.md) und [jetresessioncontext](./jetresetsessioncontext-function.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a1434-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="a1434-162">Die Datenbank-Engine unterstützt auch Transaktions Schema Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a1434-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="a1434-163">Beispielsweise ist es möglich, eine neue Transaktion zu starten, eine Tabelle zu erstellen, einige Spalten hinzuzufügen, einen Index zu erstellen oder zwei zu erstellen und dann die Transaktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a1434-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="a1434-164">Die soeben hinzugefügten Schema Elemente werden aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="a1434-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="a1434-165">Es ist auch möglich, Schema Änderungen und normale Datenbankupdates in derselben Transaktion zu mischen.</span><span class="sxs-lookup"><span data-stu-id="a1434-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a1434-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1434-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1434-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a1434-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a1434-168">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a1434-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a1434-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a1434-170">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a1434-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1434-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a1434-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a1434-172">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a1434-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1434-173"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a1434-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a1434-174">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a1434-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1434-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a1434-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a1434-176">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a1434-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a1434-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1434-177">See Also</span></span>

[<span data-ttu-id="a1434-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a1434-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a1434-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a1434-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a1434-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a1434-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a1434-181">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="a1434-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="a1434-182">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="a1434-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="a1434-183">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="a1434-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="a1434-184">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="a1434-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a1434-185">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="a1434-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="a1434-186">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="a1434-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="a1434-187">System Parameter</span><span class="sxs-lookup"><span data-stu-id="a1434-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
