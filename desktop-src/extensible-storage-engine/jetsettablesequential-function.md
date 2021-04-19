---
description: 'Weitere Informationen zu: jetsettablesequential-Funktion'
title: Jetsettablesequential-Funktion
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348359"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="9851d-103">Jetsettablesequential-Funktion</span><span class="sxs-lookup"><span data-stu-id="9851d-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="9851d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9851d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="9851d-105">Jetsettablesequential-Funktion</span><span class="sxs-lookup"><span data-stu-id="9851d-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="9851d-106">Die **jetsettablesequential** -Funktion benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten aktuellen Index scannt, der einen bestimmten Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="9851d-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="9851d-107">Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="9851d-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="9851d-108">**Windows XP:**  **jetsettablesequential** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9851d-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9851d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9851d-109">Parameters</span></span>

<span data-ttu-id="9851d-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="9851d-110">*sesid*</span></span>

<span data-ttu-id="9851d-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9851d-111">The session to use for this call.</span></span>

<span data-ttu-id="9851d-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="9851d-112">*tableid*</span></span>

<span data-ttu-id="9851d-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9851d-113">The cursor to use for this call.</span></span>

<span data-ttu-id="9851d-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9851d-114">*grbit*</span></span>

<span data-ttu-id="9851d-115">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="9851d-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9851d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9851d-116">Value</span></span></p></th>
<th><p><span data-ttu-id="9851d-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9851d-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9851d-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="9851d-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="9851d-119">Diese Option wird verwendet, um in Vorwärtsrichtung zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="9851d-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="9851d-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9851d-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9851d-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="9851d-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="9851d-122">Diese Option wird verwendet, um rückwärts zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="9851d-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="9851d-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9851d-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9851d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9851d-124">Return Value</span></span>

<span data-ttu-id="9851d-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="9851d-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9851d-126">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9851d-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9851d-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9851d-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="9851d-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9851d-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9851d-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9851d-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9851d-130">Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der-Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>stillgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="9851d-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9851d-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9851d-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9851d-132">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="9851d-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9851d-133"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9851d-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9851d-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9851d-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9851d-135">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9851d-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9851d-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9851d-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9851d-137">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9851d-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9851d-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9851d-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9851d-139">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="9851d-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9851d-140">Wenn diese Funktion erfolgreich ausgeführt wird, wird der aktuelle Index des Cursors für einen sequenziellen Scan des gesamten Indexes optimiert.</span><span class="sxs-lookup"><span data-stu-id="9851d-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="9851d-141">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="9851d-141">No change to the database state will occur.</span></span>

<span data-ttu-id="9851d-142">Wenn diese Funktion fehlschlägt, erfolgt keine Änderung an der Konfiguration des Cursors.</span><span class="sxs-lookup"><span data-stu-id="9851d-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="9851d-143">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="9851d-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9851d-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9851d-144">Remarks</span></span>

<span data-ttu-id="9851d-145">Wenn die Anwendung eine bekannte Teilmenge eines Indexes effizient scannen muss, wird eine ähnliche Optimierung auch immer dann durchgeführt, wenn ein Index Bereich mithilfe von [jetsetindexrange](./jetsetindexrange-function.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9851d-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="9851d-146">Diese Optimierung ist nur unter Windows XP und höheren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9851d-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="9851d-147">Wenn die Anwendung eine unbekannte Teilmenge eines Indexes effizient scannen muss, sollte keine Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9851d-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="9851d-148">Die Engine kann das Scan Verhalten automatisch erkennen und Daten im Voraus abrufen.</span><span class="sxs-lookup"><span data-stu-id="9851d-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="9851d-149">Dieses Verhalten ist jedoch nicht so aggressiv.</span><span class="sxs-lookup"><span data-stu-id="9851d-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="9851d-150">Durch diese Optimierung wird das Scannen des primären Indexes effizient und das Scannen nur der Index Eintrags Daten in einem sekundären Index effizient durchsucht.</span><span class="sxs-lookup"><span data-stu-id="9851d-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="9851d-151">Es wird nicht überprüft, dass ein sekundärer Index gescannt wird, während Daten Satz Daten effizient abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9851d-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="9851d-152">Dies liegt daran, dass die Engine für die Daten Satz Daten keinen Lesevorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="9851d-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9851d-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9851d-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9851d-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9851d-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9851d-155">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9851d-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9851d-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9851d-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9851d-157">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9851d-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9851d-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9851d-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9851d-159">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9851d-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9851d-160"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="9851d-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9851d-161">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9851d-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9851d-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9851d-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9851d-163">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9851d-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9851d-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9851d-164">See Also</span></span>

[<span data-ttu-id="9851d-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9851d-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9851d-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9851d-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9851d-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9851d-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9851d-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9851d-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9851d-169">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="9851d-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="9851d-170">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="9851d-170">JetStopService</span></span>](./jetstopservice-function.md)
