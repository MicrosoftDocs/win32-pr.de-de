---
description: 'Weitere Informationen zu: jetrenamecolenn-Funktion'
title: Jetrenamecolenn-Funktion
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364200"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="18674-103">Jetrenamecolenn-Funktion</span><span class="sxs-lookup"><span data-stu-id="18674-103">JetRenameColumn Function</span></span>


<span data-ttu-id="18674-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18674-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="18674-105">Jetrenamecolenn-Funktion</span><span class="sxs-lookup"><span data-stu-id="18674-105">JetRenameColumn Function</span></span>

<span data-ttu-id="18674-106">Die **jetrenamecolumn** -Funktion kann verwendet werden, um den Namen einer vorhandenen Spalte in einer Tabelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="18674-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="18674-107">**Windows XP:**  **jetrenamecolumschlag** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="18674-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="18674-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="18674-108">Parameters</span></span>

<span data-ttu-id="18674-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="18674-109">*sesid*</span></span>

<span data-ttu-id="18674-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18674-110">The session to use for this call.</span></span>

<span data-ttu-id="18674-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="18674-111">*tableid*</span></span>

<span data-ttu-id="18674-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="18674-112">The cursor to use for this call.</span></span>

<span data-ttu-id="18674-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="18674-113">*szName*</span></span>

<span data-ttu-id="18674-114">Der aktuelle Name der Spalte, die umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="18674-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="18674-115">*sznamenew*</span><span class="sxs-lookup"><span data-stu-id="18674-115">*szNameNew*</span></span>

<span data-ttu-id="18674-116">Der neue Name der Spalte, die umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="18674-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="18674-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="18674-117">*grbit*</span></span>

<span data-ttu-id="18674-118">Dieser Parameter muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="18674-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="18674-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18674-119">Return Value</span></span>

<span data-ttu-id="18674-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="18674-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="18674-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="18674-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18674-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="18674-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="18674-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18674-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18674-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="18674-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="18674-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="18674-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="18674-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="18674-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="18674-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="18674-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="18674-129">Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="18674-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="18674-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="18674-131">Einer der angegebenen Objektnamen war ungültig.</span><span class="sxs-lookup"><span data-stu-id="18674-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="18674-132">Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="18674-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="18674-133">Nachfolgend sind diese Regeln aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="18674-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="18674-134">Objektnamen müssen aus ASCII-Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="18674-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="18674-135">Objektnamen müssen mindestens ein Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="18674-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="18674-136">Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="18674-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="18674-137">Objektnamen dürfen nicht mit einem Leerzeichen beginnen. Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</span><span class="sxs-lookup"><span data-stu-id="18674-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="18674-138">Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</span><span class="sxs-lookup"><span data-stu-id="18674-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="18674-139">Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="18674-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="18674-140">Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="18674-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="18674-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="18674-142">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="18674-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="18674-143">Dies kann bei <strong>jetrenamecolumschlag</strong> vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="18674-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="18674-144"><em>szName</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="18674-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="18674-145"><em>sznamenew</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="18674-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="18674-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="18674-147">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="18674-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="18674-148">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18674-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="18674-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="18674-150">Dieser Vorgang kann nur ausgeführt werden, wenn die Sitzung derzeit nicht innerhalb einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18674-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="18674-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="18674-152">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18674-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="18674-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="18674-154">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18674-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="18674-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="18674-156">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18674-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="18674-157">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18674-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="18674-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="18674-159">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="18674-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="18674-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="18674-161">Ein Update kann nicht innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="18674-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="18674-162">Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="18674-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="18674-163">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18674-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18674-164">Bei Erfolg wird der Name der angegebenen Spalte in der Tabelle, die dem Cursor zugeordnet ist, dauerhaft in den neuen Namen geändert.</span><span class="sxs-lookup"><span data-stu-id="18674-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="18674-165">Alle Indizes, die auf diese Spalte verweisen, werden ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="18674-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="18674-166">Bei einem Fehler tritt keine Änderung am Daten Bank Status auf.</span><span class="sxs-lookup"><span data-stu-id="18674-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="18674-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18674-167">Remarks</span></span>

<span data-ttu-id="18674-168">Der Spalten Umbenennungs Vorgang ist ungewöhnlich, weil er im Gegensatz zu anderen Schema Vorgängen nicht als Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18674-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="18674-169">Wenn eine Spalte in einer bestimmten Tabelle in einer Sitzung umbenannt wird, wird die Änderung in allen anderen Sitzungen, die diese Tabelle verwenden, sofort angezeigt, auch wenn Sie sich in einer Transaktion befinden, durch die verhindert wird, dass von der Sitzung andere Änderungen angezeigt werden, die den Umbenennungs Vorgang durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="18674-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="18674-170">Der Umbenennungs Vorgang hat keine Auswirkung auf die Spalten-ID einer Spalte.</span><span class="sxs-lookup"><span data-stu-id="18674-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="18674-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18674-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18674-172"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18674-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-173">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18674-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-174"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18674-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-175">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18674-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-176"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="18674-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-177">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="18674-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-178"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="18674-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-179">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="18674-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18674-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="18674-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-181">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="18674-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18674-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="18674-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="18674-183">Implementiert als <strong>jetrenamecolumnw</strong> (Unicode) und <strong>jetrenamecolumna</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="18674-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="18674-184">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18674-184">See Also</span></span>

[<span data-ttu-id="18674-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="18674-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="18674-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="18674-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="18674-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="18674-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="18674-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="18674-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="18674-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="18674-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
