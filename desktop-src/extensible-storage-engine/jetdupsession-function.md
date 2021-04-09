---
description: 'Weitere Informationen zu: jetdupsession-Funktion'
title: Jetdupsession-Funktion
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867552"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="3b38f-103">Jetdupsession-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b38f-103">JetDupSession Function</span></span>


<span data-ttu-id="3b38f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3b38f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="3b38f-105">Jetdupsession-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b38f-105">JetDupSession Function</span></span>

<span data-ttu-id="3b38f-106">Die **jetdupsession** -Funktion startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungs handle ([JET_SESID](./jet-sesid.md)) zurück.</span><span class="sxs-lookup"><span data-stu-id="3b38f-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="3b38f-107">Sitzungen steuern den gesamten Zugriff auf die Datenbank und werden verwendet, um den Umfang der Transaktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="3b38f-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="3b38f-108">Die Sitzung kann verwendet werden, um Transaktionen zu starten, zu übertragen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="3b38f-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="3b38f-109">Die Sitzung wird auch zum Anfügen, erstellen oder Öffnen einer Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b38f-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="3b38f-110">Die Sitzung wird als Kontext für alle DDL-und DML-Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b38f-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="3b38f-111">Um Parallelität und parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3b38f-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="3b38f-112">**Hinweis** Diese API verhält sich auf alle Arten, als [jetbeginsession](./jetbeginsession-function.md) , die für die Instanz der Sitzung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b38f-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="3b38f-113">Diese Funktion wird nicht empfohlen, [jetbeginsession](./jetbeginsession-function.md) wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="3b38f-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="3b38f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b38f-114">Parameters</span></span>

<span data-ttu-id="3b38f-115">*-sid*</span><span class="sxs-lookup"><span data-stu-id="3b38f-115">*sesid*</span></span>

<span data-ttu-id="3b38f-116">Die Sitzung, die als Quelle für das Duplizieren oder Starten der Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b38f-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="3b38f-117">*psetup-sid*</span><span class="sxs-lookup"><span data-stu-id="3b38f-117">*psesid*</span></span>

<span data-ttu-id="3b38f-118">Ein Zeiger auf die Variable, die vom Sitzungs Handle bei erfolgreicher Rückgabe initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b38f-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="3b38f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b38f-119">Return Value</span></span>

<span data-ttu-id="3b38f-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="3b38f-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3b38f-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3b38f-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b38f-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3b38f-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="3b38f-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b38f-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3b38f-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3b38f-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3b38f-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3b38f-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3b38f-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="3b38f-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3b38f-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3b38f-129">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="3b38f-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3b38f-130">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b38f-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3b38f-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3b38f-132">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b38f-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3b38f-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3b38f-134">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b38f-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="3b38f-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="3b38f-136">Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3b38f-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="3b38f-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="3b38f-138">Die Anzahl der Sitzungen, die die Engine für den Start des Clients zulässt, ist begrenzt.</span><span class="sxs-lookup"><span data-stu-id="3b38f-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="3b38f-139">Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit der <em>JET_paramMaxSessions</em> -Konstante geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3b38f-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="3b38f-140">Die Standard Anzahl von Sitzungen ist 16.</span><span class="sxs-lookup"><span data-stu-id="3b38f-140">The default number of sessions is 16.</span></span> <span data-ttu-id="3b38f-141">Weitere Informationen zu <em>JET_paramMaxSessions</em>finden Sie unter <a href="gg294139(v=exchg.10).md">System Parameter</a> .</span><span class="sxs-lookup"><span data-stu-id="3b38f-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3b38f-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b38f-143">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b38f-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3b38f-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3b38f-145">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="3b38f-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b38f-146">Bei Erfolg wird das Sitzungs Handle initialisiert und kann für Daten Bank Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b38f-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="3b38f-147">Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b38f-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3b38f-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b38f-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-149"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3b38f-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3b38f-150">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b38f-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-151"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3b38f-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3b38f-152">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3b38f-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-153"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3b38f-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3b38f-154">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3b38f-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b38f-155"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="3b38f-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3b38f-156">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3b38f-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b38f-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3b38f-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3b38f-158">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3b38f-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3b38f-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b38f-159">See Also</span></span>

[<span data-ttu-id="3b38f-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3b38f-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3b38f-161">Jetbeginsession</span><span class="sxs-lookup"><span data-stu-id="3b38f-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="3b38f-162">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="3b38f-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3b38f-163">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="3b38f-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="3b38f-164">System Parameter</span><span class="sxs-lookup"><span data-stu-id="3b38f-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
