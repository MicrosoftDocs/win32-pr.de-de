---
description: 'Weitere Informationen zu: jetrenametable-Funktion'
title: Jetrenametable-Funktion
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348768"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="58242-103">Jetrenametable-Funktion</span><span class="sxs-lookup"><span data-stu-id="58242-103">JetRenameTable Function</span></span>


<span data-ttu-id="58242-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="58242-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="58242-105">Jetrenametable-Funktion</span><span class="sxs-lookup"><span data-stu-id="58242-105">JetRenameTable Function</span></span>

<span data-ttu-id="58242-106">Die **jetrenametable** -Funktion kann verwendet werden, um den Namen einer vorhandenen Tabelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="58242-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="58242-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58242-107">Parameters</span></span>

<span data-ttu-id="58242-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="58242-108">*sesid*</span></span>

<span data-ttu-id="58242-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58242-109">The session to use for this call.</span></span>

<span data-ttu-id="58242-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="58242-110">*dbid*</span></span>

<span data-ttu-id="58242-111">Die Datenbank, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58242-111">The database to use for this call.</span></span>

<span data-ttu-id="58242-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="58242-112">*szName*</span></span>

<span data-ttu-id="58242-113">Der aktuelle Name der Tabelle, die umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="58242-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="58242-114">*sznamenew*</span><span class="sxs-lookup"><span data-stu-id="58242-114">*szNameNew*</span></span>

<span data-ttu-id="58242-115">Der neue Name für die Tabelle, die umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="58242-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="58242-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58242-116">Return Value</span></span>

<span data-ttu-id="58242-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="58242-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="58242-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="58242-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58242-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="58242-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="58242-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58242-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58242-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="58242-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="58242-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="58242-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="58242-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="58242-124">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="58242-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="58242-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="58242-126">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="58242-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="58242-127">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58242-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="58242-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="58242-129">Die angegebene Datenbank war ungültig.</span><span class="sxs-lookup"><span data-stu-id="58242-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="58242-130">Dieser Fehler wird nur in Windows 2000 zurückgegeben, wenn versucht wird, einen Tabellen Umbenennungs Vorgang für die temporäre Datenbank auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58242-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="58242-131">JET_errInvalidDatabaseId wird in späteren Versionen für diesen Fall zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58242-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="58242-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="58242-133">Die angegebene Datenbank-ID war ungültig.</span><span class="sxs-lookup"><span data-stu-id="58242-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="58242-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="58242-135">Einer der angegebenen Objektnamen war ungültig.</span><span class="sxs-lookup"><span data-stu-id="58242-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="58242-136">Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="58242-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="58242-137">Nachfolgend sind diese Regeln aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="58242-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="58242-138">Objektnamen müssen aus ASCII-Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="58242-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="58242-139">Objektnamen müssen mindestens ein Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="58242-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="58242-140">Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="58242-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="58242-141">Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="58242-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="58242-142">Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</span><span class="sxs-lookup"><span data-stu-id="58242-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="58242-143">Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten. nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="58242-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="58242-144">Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="58242-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="58242-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="58242-146">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="58242-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="58242-147">Dies kann bei <strong>jetrenametable</strong> vorkommen, wenn:</span><span class="sxs-lookup"><span data-stu-id="58242-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="58242-148"><em>szName</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="58242-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="58242-149"><em>sznamenew</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="58242-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="58242-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="58242-151">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="58242-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="58242-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="58242-153">Diese angegebene Tabelle ist für diese Datenbank nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58242-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="58242-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="58242-155">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58242-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="58242-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="58242-157">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58242-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="58242-158">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58242-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="58242-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="58242-160">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="58242-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="58242-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="58242-162">Ein Update kann nicht innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="58242-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="58242-163">Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="58242-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="58242-164">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="58242-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58242-165">Bei Erfolg wird der Name der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Namen geändert.</span><span class="sxs-lookup"><span data-stu-id="58242-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="58242-166">Bei einem Fehler tritt keine Änderung am Daten Bank Status auf.</span><span class="sxs-lookup"><span data-stu-id="58242-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="58242-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58242-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58242-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="58242-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-169">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="58242-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="58242-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-171">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="58242-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="58242-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-173">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="58242-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-174"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="58242-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-175">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="58242-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58242-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="58242-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-177">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="58242-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58242-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="58242-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="58242-179">Implementiert als <strong>jetrenametablew</strong> (Unicode) und <strong>jetrenametablea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="58242-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="58242-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58242-180">See Also</span></span>

[<span data-ttu-id="58242-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="58242-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="58242-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="58242-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="58242-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="58242-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="58242-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="58242-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
