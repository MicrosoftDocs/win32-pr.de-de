---
description: 'Weitere Informationen zu: jetbeginsession-Funktion'
title: JetBeginSession-Funktion
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351075"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="c414d-103">JetBeginSession-Funktion</span><span class="sxs-lookup"><span data-stu-id="c414d-103">JetBeginSession Function</span></span>


<span data-ttu-id="c414d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c414d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="c414d-105">JetBeginSession-Funktion</span><span class="sxs-lookup"><span data-stu-id="c414d-105">JetBeginSession Function</span></span>

<span data-ttu-id="c414d-106">Die **jetbeginsession** -Funktion startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungs handle ([JET_SESID](./jet-sesid.md)) zurück.</span><span class="sxs-lookup"><span data-stu-id="c414d-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="c414d-107">Sitzungen steuern den gesamten Zugriff auf die Datenbank und werden verwendet, um den Umfang der Transaktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c414d-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="c414d-108">Die Sitzung kann verwendet werden, um Transaktionen zu starten, zu übertragen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="c414d-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="c414d-109">Die Sitzung wird auch zum Anfügen, erstellen oder Öffnen einer Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="c414d-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="c414d-110">Die Sitzung wird als Kontext für alle DDL-und DML-Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="c414d-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="c414d-111">Um Parallelität und parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="c414d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c414d-112">Parameters</span></span>

<span data-ttu-id="c414d-113">*lichen*</span><span class="sxs-lookup"><span data-stu-id="c414d-113">*instance*</span></span>

<span data-ttu-id="c414d-114">Die Daten Bank Instanz, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c414d-114">The database instance to use for this call.</span></span>

<span data-ttu-id="c414d-115">*psetup-sid*</span><span class="sxs-lookup"><span data-stu-id="c414d-115">*psesid*</span></span>

<span data-ttu-id="c414d-116">Ein Zeiger auf die Variable, die vom Sitzungs Handle bei erfolgreicher Rückgabe initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c414d-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="c414d-117">*szusername*</span><span class="sxs-lookup"><span data-stu-id="c414d-117">*szUserName*</span></span>

<span data-ttu-id="c414d-118">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="c414d-118">This parameter is reserved.</span></span>

<span data-ttu-id="c414d-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="c414d-119">*szPassword*</span></span>

<span data-ttu-id="c414d-120">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="c414d-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="c414d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c414d-121">Return Value</span></span>

<span data-ttu-id="c414d-122">Diese Funktion ermöglicht die Rückgabe von [JET_ERR](./jet-err.md)s, die in dieser API definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c414d-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="c414d-123">Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c414d-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c414d-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c414d-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="c414d-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c414d-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c414d-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c414d-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c414d-127">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c414d-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c414d-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c414d-129">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c414d-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c414d-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c414d-131">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="c414d-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c414d-132">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c414d-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c414d-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c414d-134">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="c414d-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c414d-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c414d-136">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c414d-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c414d-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c414d-138">Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c414d-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="c414d-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="c414d-140">Die Anzahl der Sitzungen, die die Engine für den Start des Clients zulässt, ist begrenzt.</span><span class="sxs-lookup"><span data-stu-id="c414d-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="c414d-141">Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit der JET_paramMaxSessions-Konstante geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="c414d-142">Die Standard Anzahl von Sitzungen ist 16.</span><span class="sxs-lookup"><span data-stu-id="c414d-142">The default number of sessions is 16.</span></span> <span data-ttu-id="c414d-143">Weitere Informationen zu JET_paramMaxSessions finden Sie unter <a href="gg294139(v=exchg.10).md">System Parameter</a> .</span><span class="sxs-lookup"><span data-stu-id="c414d-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c414d-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c414d-145">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c414d-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c414d-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c414d-147">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c414d-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c414d-148">Bei Erfolg wird das Sitzungs Handle initialisiert und kann für Daten Bank Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="c414d-149">Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c414d-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c414d-150">Remarks</span></span>

<span data-ttu-id="c414d-151">Bei der Verwendung von Sitzungen über verschiedene Threads muss sorgfältig vorgegangen werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="c414d-152">In einer Sitzung wird nachverfolgt, in welchem Thread Sie während [jetbegintransaction](./jetbegintransaction-function.md), [jetcommittransaction](./jetcommittransaction-function.md)oder [jetrollback](./jetrollback-function.md)verwendet wurde, und es wird ein Fehler ausgelöst, wenn Sie für mehrere Threads mit einer geöffneten Transaktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c414d-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="c414d-153">Das [jetresessioncontext](./jetresetsessioncontext-function.md)-Objekt [kann dieses](./jetsetsessioncontext-function.md) Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="c414d-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="c414d-154">Da es sich bei der Sitzung immer noch um einen serialisierten Kontext handelt, können mehrere Daten Bank Vorgänge nicht gleichzeitig in einer einzelnen Sitzung ausgeführt werden, sondern nur seriell.</span><span class="sxs-lookup"><span data-stu-id="c414d-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="c414d-155">Sie können jedoch mehrere-Sitzungen verwenden, um gleichzeitigen Datenbankzugriff zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="c414d-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="c414d-156">Sitzungen können innerhalb einer Transaktion Thread übergreifend verwendet werden, indem Sie die Sitzungs Kontexte festlegen und zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="c414d-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="c414d-157">Das Sitzungs Handle muss mit [jetendsession](./jetendsession-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c414d-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c414d-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c414d-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c414d-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-160">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c414d-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-162">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c414d-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-164">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c414d-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-165"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-166">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c414d-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c414d-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-168">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c414d-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c414d-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c414d-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c414d-170">Implementiert als <strong>jetbeginsessionw</strong> (Unicode) und <strong>jetbeginsessiona</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c414d-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c414d-171">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c414d-171">See Also</span></span>

[<span data-ttu-id="c414d-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c414d-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c414d-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c414d-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c414d-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c414d-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c414d-175">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="c414d-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="c414d-176">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="c414d-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="c414d-177">Jetdupsession</span><span class="sxs-lookup"><span data-stu-id="c414d-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="c414d-178">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="c414d-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="c414d-179">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="c414d-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="c414d-180">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="c414d-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="c414d-181">Jetabessioncontext</span><span class="sxs-lookup"><span data-stu-id="c414d-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="c414d-182">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="c414d-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c414d-183">System Parameter</span><span class="sxs-lookup"><span data-stu-id="c414d-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
