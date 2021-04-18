---
description: Weitere Informationen finden Sie in der jetabessioncontext-Funktion
title: Jetabessioncontext-Funktion
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345762"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="06b7f-103">Jetabessioncontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="06b7f-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="06b7f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06b7f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="06b7f-105">Jetabessioncontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="06b7f-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="06b7f-106">Die **jetsetsessioncontext** -Funktion verknüpft eine Sitzung mit dem aktuellen Thread unter Verwendung des angegebenen Kontext Handles.</span><span class="sxs-lookup"><span data-stu-id="06b7f-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="06b7f-107">Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im gleichen Thread ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="06b7f-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="06b7f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06b7f-108">Parameters</span></span>

<span data-ttu-id="06b7f-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="06b7f-109">*sesid*</span></span>

<span data-ttu-id="06b7f-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06b7f-110">The session to use for this call.</span></span>

<span data-ttu-id="06b7f-111">*ulcontext*</span><span class="sxs-lookup"><span data-stu-id="06b7f-111">*ulContext*</span></span>

<span data-ttu-id="06b7f-112">Ein eindeutiger Bezeichner, dem diese Sitzung zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="06b7f-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="06b7f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06b7f-113">Return Value</span></span>

<span data-ttu-id="06b7f-114">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="06b7f-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="06b7f-115">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="06b7f-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06b7f-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="06b7f-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="06b7f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06b7f-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="06b7f-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="06b7f-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="06b7f-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="06b7f-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="06b7f-121">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="06b7f-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="06b7f-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="06b7f-123">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="06b7f-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="06b7f-124"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06b7f-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="06b7f-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="06b7f-126">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06b7f-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="06b7f-127">Dieser Fehler wird von <strong>jetin</strong> den folgenden Bedingungen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="06b7f-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="06b7f-128"><em>ulcontext</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="06b7f-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="06b7f-129"><em>ulcontext</em> ist-1</span><span class="sxs-lookup"><span data-stu-id="06b7f-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="06b7f-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="06b7f-131">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="06b7f-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="06b7f-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="06b7f-133">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06b7f-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="06b7f-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="06b7f-135">Die Sitzung konnte dem aktuellen Thread nicht zugeordnet werden, da Sie bereits einem Thread zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="06b7f-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="06b7f-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="06b7f-137">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="06b7f-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06b7f-138">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Sitzung dem aktuellen Thread zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="06b7f-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="06b7f-139">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="06b7f-139">No change to the database state will occur.</span></span>

<span data-ttu-id="06b7f-140">Wenn diese Funktion fehlschlägt, bleibt der Sitzungszustand unverändert.</span><span class="sxs-lookup"><span data-stu-id="06b7f-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="06b7f-141">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="06b7f-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="06b7f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06b7f-142">Remarks</span></span>

<span data-ttu-id="06b7f-143">Eine Sitzung wird in der Regel an einen bestimmten Thread für die Dauer einer Transaktion gebunden.</span><span class="sxs-lookup"><span data-stu-id="06b7f-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="06b7f-144">Dieses Verhalten soll Anwendungen dabei helfen, die konzeptionell beschädigte Freigabe einer einzelnen Sitzung unter mehreren Threads zu erkennen und zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="06b7f-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="06b7f-145">Manchmal funktioniert diese einfache Überprüfung nicht mit der Architektur der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="06b7f-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="06b7f-146">Wenn die Anwendung z. b. serverseitige Objekte mithilfe eines Thread Pools hostet und Transaktionen mehrere Server Aufrufe an ein bestimmtes Objekt überspannen, kann dieser Schutz dazu führen, dass einige dieser Aufrufe mit JET_errSessionSharingViolation fehlschlagen, obwohl das Verwendungs Muster korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="06b7f-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="06b7f-147">Diese Situation tritt häufig bei COM-Objekt Servern auf.</span><span class="sxs-lookup"><span data-stu-id="06b7f-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="06b7f-148">**Jetabsitzungskontext** und [jetressitzungskontext](./jetresetsessioncontext-function.md) lösen dieses Problem, indem Sie die Überprüfung dieser Sitzung ein wenig flexibler gestalten.</span><span class="sxs-lookup"><span data-stu-id="06b7f-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="06b7f-149">Wenn die Anwendung mit einer bestimmten Sitzung eine Reihe von ESE-API-aufrufen durchführen soll, wird der Sitzungs Kontext zuerst auf einen bestimmten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06b7f-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="06b7f-150">Durch diese Aktion wird die Sitzung dem aufrufenden Thread zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="06b7f-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="06b7f-151">Im vorliegenden Beispiel könnte dieser Kontext die Adresse des Objekts sein, das das Jet-Sitzungs Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="06b7f-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="06b7f-152">Nachdem die ESE-API-Aufrufe durchgeführt wurden, setzt die Anwendung den Sitzungs Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="06b7f-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="06b7f-153">Durch diese Aktion wird die Zuordnung der Sitzung zum aufrufenden Thread aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="06b7f-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="06b7f-154">Das-Objekt und seine Sitzung können dann von einem anderen Thread verwendet werden, auch wenn die Sitzung über eine aktive Transaktion verfügt.</span><span class="sxs-lookup"><span data-stu-id="06b7f-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="06b7f-155">Es ist wichtig zu beachten, dass **jetctessioncontext** aufgerufen werden muss, bevor eine Transaktion in dieser Sitzung geöffnet wird, oder die Zuordnung funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="06b7f-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="06b7f-156">**Jetsezessioncontext** ist Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="06b7f-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="06b7f-157">Mehrere Threads können gleichzeitig versuchen, einen Thread Kontext in derselben Sitzung festzulegen, und nur ein Thread wird gewonnen.</span><span class="sxs-lookup"><span data-stu-id="06b7f-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="06b7f-158">Diese Tatsache kann von der Anwendung verwendet werden, um eine Sitzung aus einem Pool zuzuordnen, ohne dass der externe Zustand über die Zuordnung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="06b7f-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="06b7f-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06b7f-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-160"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="06b7f-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06b7f-161">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="06b7f-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="06b7f-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06b7f-163">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="06b7f-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-164"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="06b7f-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06b7f-165">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="06b7f-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06b7f-166"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="06b7f-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="06b7f-167">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="06b7f-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06b7f-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="06b7f-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="06b7f-169">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="06b7f-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="06b7f-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06b7f-170">See Also</span></span>

[<span data-ttu-id="06b7f-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="06b7f-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="06b7f-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="06b7f-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="06b7f-173">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="06b7f-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="06b7f-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="06b7f-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="06b7f-175">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="06b7f-175">JetStopService</span></span>](./jetstopservice-function.md)
