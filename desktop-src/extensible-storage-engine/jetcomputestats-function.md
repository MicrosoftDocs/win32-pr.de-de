---
description: 'Weitere Informationen finden Sie unter: jetcomputestats-Funktion'
title: Jetcomputestats-Funktion
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218590"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="c8cbf-103">Jetcomputestats-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8cbf-103">JetComputeStats Function</span></span>


<span data-ttu-id="c8cbf-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c8cbf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="c8cbf-105">Jetcomputestats-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8cbf-105">JetComputeStats Function</span></span>

<span data-ttu-id="c8cbf-106">Die **jetcomputestats** -Funktion durchläuft jeden Index einer Tabelle, um genau die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="c8cbf-107">Diese Informationen werden in Verbindung mit der Anzahl von Datenbankseiten, die für einen Index zugeordnet sind, und dem aktuellen Zeitpunkt der Berechnung in den Index Metadaten in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="c8cbf-108">Diese Daten können anschließend mit Informations Vorgängen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="c8cbf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8cbf-109">Parameters</span></span>

<span data-ttu-id="c8cbf-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="c8cbf-110">*sesid*</span></span>

<span data-ttu-id="c8cbf-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-111">The session to use for this call.</span></span>

<span data-ttu-id="c8cbf-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c8cbf-112">*tableid*</span></span>

<span data-ttu-id="c8cbf-113">Der Cursor, der für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="c8cbf-114">Beschreibt die Tabelle, für die Statistiken berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="c8cbf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8cbf-115">Return Value</span></span>

<span data-ttu-id="c8cbf-116">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c8cbf-117">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c8cbf-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8cbf-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c8cbf-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c8cbf-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8cbf-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c8cbf-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-121">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c8cbf-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-123">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c8cbf-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-125">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c8cbf-126">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c8cbf-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-128">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c8cbf-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-130">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="c8cbf-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-132">Es ist ein Fehler aufgetreten, der erfordert, dass für diesen Vorgang alle Änderungen zurückgesetzt werden, das Transaktionsrollback selbst jedoch fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="c8cbf-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c8cbf-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-134">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c8cbf-135">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c8cbf-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c8cbf-137">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8cbf-138">Bei Erfolg werden aktuelle Statistiken in den Daten Bank Katalogen für die Tabelle gespeichert, die mit dem angegebenen Cursor beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="c8cbf-139">Bei einem Fehler werden keine Updates jeglicher Art an der Datenbank vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c8cbf-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8cbf-140">Remarks</span></span>

<span data-ttu-id="c8cbf-141">Dieser Vorgang kann Ressourcen aufwendig sein, da jeder Index in einer Tabelle vollständig durchlaufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="c8cbf-142">[Jetgetrecordposition](./jetgetrecordposition-function.md) kann verwendet werden, um eine grobe Schätzung der Anzahl von Einträgen in einem Index zu erhalten, kann jedoch nicht die Anzahl der unterschiedlichen Werte in einem Index schätzen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="c8cbf-143">Die von diesem Vorgang berechneten Daten werden veraltet, und die Tabelle wird anschließend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="c8cbf-144">Aktualisierungen der von **jetcomputestats** vorgenommenen Datenbank werden verzögert durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="c8cbf-145">Dies bedeutet, dass keine Protokoll Leerung von diesem Vorgang begleitet wird und ein Systemabsturz nach einer Rückgabe von JET_errSuccess von **jetcomputestats** weiterhin dazu führen kann, dass diese Updates verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c8cbf-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8cbf-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c8cbf-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c8cbf-148">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c8cbf-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c8cbf-150">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c8cbf-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c8cbf-152">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8cbf-153"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c8cbf-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c8cbf-154">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8cbf-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c8cbf-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c8cbf-156">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c8cbf-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c8cbf-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8cbf-157">See Also</span></span>

[<span data-ttu-id="c8cbf-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c8cbf-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c8cbf-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c8cbf-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c8cbf-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c8cbf-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c8cbf-161">Jetgetrecordposition</span><span class="sxs-lookup"><span data-stu-id="c8cbf-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="c8cbf-162">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="c8cbf-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="c8cbf-163">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="c8cbf-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="c8cbf-164">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="c8cbf-164">JetStopService</span></span>](./jetstopservice-function.md)
