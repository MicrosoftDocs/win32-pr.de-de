---
description: Weitere Informationen finden Sie in der jetsetcolumndefaultvalue-Funktion.
title: Jetsetcolumndefaultvalue-Funktion
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862196"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="8c5d8-103">Jetsetcolumndefaultvalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c5d8-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="8c5d8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c5d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="8c5d8-105">Jetsetcolumndefaultvalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c5d8-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="8c5d8-106">Die **jetsetcolumndefaultvalue** -Funktion kann verwendet werden, um den Standardwert einer vorhandenen Spalte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8c5d8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c5d8-107">Parameters</span></span>

<span data-ttu-id="8c5d8-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-108">*sesid*</span></span>

<span data-ttu-id="8c5d8-109">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-109">The session to use for this call.</span></span>

<span data-ttu-id="8c5d8-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-110">*dbid*</span></span>

<span data-ttu-id="8c5d8-111">Die Datenbank, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-111">The database to use for this call.</span></span>

<span data-ttu-id="8c5d8-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-112">*szTableName*</span></span>

<span data-ttu-id="8c5d8-113">Der Name der Tabelle, in der die betroffene Spalte enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="8c5d8-114">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-114">*szColumnName*</span></span>

<span data-ttu-id="8c5d8-115">Der Name der Spalte, deren Standardwert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="8c5d8-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-116">*pvData*</span></span>

<span data-ttu-id="8c5d8-117">Der Eingabepuffer, der den neuen Standardwert enthält.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="8c5d8-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-118">*cbData*</span></span>

<span data-ttu-id="8c5d8-119">Die Größe des Eingabe Puffers, der den neuen Standardwert enthält.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="8c5d8-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8c5d8-120">*grbit*</span></span>

<span data-ttu-id="8c5d8-121">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="8c5d8-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c5d8-122">Return Value</span></span>

<span data-ttu-id="8c5d8-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8c5d8-124">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8c5d8-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c5d8-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8c5d8-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="8c5d8-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c5d8-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8c5d8-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8c5d8-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-130">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="8c5d8-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-132">Identisch mit JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="8c5d8-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-134">Diese angegebene Spalte wird derzeit von einem Index verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="8c5d8-135"><strong>Jetsetcolumndefaultvalue</strong> kann den Standardwert einer Spalte, auf die in der Definition eines Indexes verwiesen wird, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="8c5d8-136">Dies liegt daran, dass dadurch der Inhalt des Indexes geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="8c5d8-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-138">Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8c5d8-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-140">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8c5d8-141">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="8c5d8-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-143">Die angegebene Datenbank-ID war ungültig.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="8c5d8-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-145">Einer der angegebenen Objektnamen war ungültig.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="8c5d8-146">Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="8c5d8-147">Nachfolgend sind diese Regeln aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8c5d8-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c5d8-148">Objektnamen müssen aus ASCII-Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-149">Objektnamen müssen mindestens ein Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-150">Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-151">Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-152">Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-153">Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-154">Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="8c5d8-155">Dies bedeutet, dass Objektnamen keines der Leerzeichen enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8c5d8-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-157">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="8c5d8-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-159">Die Spalte konnte nicht auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-159">The column could not be set to NULL.</span></span> <span data-ttu-id="8c5d8-160">Dies geschieht für <strong>jetsetcolumndefaultvalue</strong> in folgenden Fällen:</span><span class="sxs-lookup"><span data-stu-id="8c5d8-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c5d8-161"><em>cbData</em> ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8c5d8-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="8c5d8-162"><strong>pvData</strong> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="8c5d8-163">Daher ist es nicht möglich, den Standardwert einer Spalte (zurück) auf NULL oder auf einen Wert der Länge 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="8c5d8-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-165">Diese angegebene Tabelle ist für diese Datenbank nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8c5d8-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-167">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8c5d8-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-169">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="8c5d8-170">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="8c5d8-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-172">Diese angegebene Tabelle wird von einer anderen Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="8c5d8-173"><strong>Jetsetcolumndefaultvalue</strong> erfordert exklusiven Zugriff auf eine Tabelle, um den Standardwert der Spalte für Releases vor Windows Server 2003 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8c5d8-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-175">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="8c5d8-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-177">Es ist nicht zulässig, ein Update zu versuchen, wenn es innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion liegt.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="8c5d8-178">Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="8c5d8-179">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="8c5d8-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="8c5d8-181">Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="8c5d8-182">Das von dieser Sitzung versuchte Update schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c5d8-183">Bei Erfolg wird der Standardwert der angegebenen Spalte in der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Standardwert geändert.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="8c5d8-184">Bei einem Fehler tritt keine Änderung am Daten Bank Status auf.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8c5d8-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c5d8-185">Remarks</span></span>

<span data-ttu-id="8c5d8-186">Es ist nicht möglich, den Standardwert einer Spalte in einer Vorlagen Tabelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="8c5d8-187">Der Standardwert einer Spalte wird von der Datenbank-Engine für lange Text-und lange Binär Spalten automatisch auf 255 Byte gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8c5d8-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c5d8-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-190">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-192">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-194">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-195"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-196">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5d8-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-198">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8c5d8-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5d8-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8c5d8-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5d8-200">Implementiert als <strong>jetsetcolumndefaultvaluew</strong> (Unicode) und <strong>jetsetcolumndefaultvaluea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8c5d8-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8c5d8-201">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8c5d8-201">See Also</span></span>

[<span data-ttu-id="8c5d8-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="8c5d8-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="8c5d8-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8c5d8-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8c5d8-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8c5d8-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8c5d8-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8c5d8-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8c5d8-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="8c5d8-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="8c5d8-207">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="8c5d8-207">JetStopService</span></span>](./jetstopservice-function.md)
