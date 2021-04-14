---
description: 'Weitere Informationen zu: jetunregistercallback-Funktion'
title: Jetunregistercallback-Funktion
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b342bab655e3cf1e3c1a5967410edb1c971af87b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393470"
---
# <a name="jetunregistercallback-function"></a><span data-ttu-id="c6e62-103">Jetunregistercallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6e62-103">JetUnregisterCallback Function</span></span>


<span data-ttu-id="c6e62-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c6e62-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetunregistercallback-function"></a><span data-ttu-id="c6e62-105">Jetunregistercallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6e62-105">JetUnregisterCallback Function</span></span>

<span data-ttu-id="c6e62-106">Die **jetunregistercallback** -Funktion ermöglicht es der Anwendung, die Datenbank-Engine so zu konfigurieren, dass die Ausgabe von Benachrichtigungen an die Anwendung nicht mehr wie zuvor durch [jetregistercallback](./jetregistercallback-function.md)angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6e62-106">The **JetUnregisterCallback** function enables the application to configure the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

<span data-ttu-id="c6e62-107">**Windows XP:**  **jetunregistercallback** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e62-107">**Windows XP:**  **JetUnregisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="c6e62-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6e62-108">Parameters</span></span>

<span data-ttu-id="c6e62-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="c6e62-109">*sesid*</span></span>

<span data-ttu-id="c6e62-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e62-110">The session to use for this call.</span></span>

<span data-ttu-id="c6e62-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c6e62-111">*tableid*</span></span>

<span data-ttu-id="c6e62-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e62-112">The cursor to use for this call.</span></span>

<span data-ttu-id="c6e62-113">*cbyp*</span><span class="sxs-lookup"><span data-stu-id="c6e62-113">*cbtyp*</span></span>

<span data-ttu-id="c6e62-114">Eine Bitmaske, die aus den Rückruf Gründen besteht, dass die Anwendung keine Benachrichtigungen mehr empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="c6e62-114">A bitmask composed of the callback reasons that the application no longer wishes to receive notifications.</span></span>

<span data-ttu-id="c6e62-115">Um diese Bitmaske zu erstellen, führen Sie einfach oder zusammengültige Rückruf Gründe aus der [JET_CBTYP](./jet-cbtyp.md) Enumeration aus.</span><span class="sxs-lookup"><span data-stu-id="c6e62-115">To create this bitmask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="c6e62-116">*hcallbackid*</span><span class="sxs-lookup"><span data-stu-id="c6e62-116">*hCallbackId*</span></span>

<span data-ttu-id="c6e62-117">Das Handle des registrierten Rückrufs, der von [jetregistercallback](./jetregistercallback-function.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c6e62-117">The handle of the registered callback that was returned by [JetRegisterCallback](./jetregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="c6e62-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6e62-118">Return Value</span></span>

<span data-ttu-id="c6e62-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c6e62-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c6e62-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c6e62-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6e62-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c6e62-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="c6e62-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e62-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c6e62-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c6e62-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c6e62-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e62-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c6e62-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c6e62-126">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c6e62-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c6e62-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c6e62-128">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="c6e62-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c6e62-129"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e62-129"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e62-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c6e62-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c6e62-131">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6e62-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c6e62-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c6e62-133">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6e62-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e62-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c6e62-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c6e62-135">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6e62-135">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c6e62-136"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e62-136"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c6e62-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c6e62-138">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c6e62-138">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6e62-139">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Registrierung des angegebenen Rückrufs für die angegebenen Rückruf Gründe mit der Tabelle aufgehoben, die dem angegebenen Cursor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c6e62-139">If this function succeeds, the specified callback will be unregistered for the given callback reasons with the table that is associated with the given cursor.</span></span> <span data-ttu-id="c6e62-140">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="c6e62-140">No change to the database state will occur.</span></span>

<span data-ttu-id="c6e62-141">Wenn diese Funktion fehlschlägt, wird die Registrierung des angegebenen Rückrufs nicht aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c6e62-141">If this function fails, the specified callback will not be unregistered.</span></span> <span data-ttu-id="c6e62-142">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="c6e62-142">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c6e62-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6e62-143">Remarks</span></span>

<span data-ttu-id="c6e62-144">Die angegebene Bitmaske sollte genau mit der Bitmaske übereinstimmen, die beim Registrieren des Rückrufs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6e62-144">The given bitmask should exactly match the bitmask that is specified when registering the callback.</span></span> <span data-ttu-id="c6e62-145">Das Entfernen einer Teilmenge dieser Benachrichtigungen wird von der Datenbank-Engine derzeit nicht unterstützt, und es wird kein Fehler zurückgegeben, wenn ein Versuch unternommen wird.</span><span class="sxs-lookup"><span data-stu-id="c6e62-145">The database engine does not currently support removing a subset of these notifications and it does not return an error when this is attempted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c6e62-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e62-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-147"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c6e62-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e62-148">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6e62-148">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e62-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c6e62-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e62-150">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6e62-150">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c6e62-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e62-152">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c6e62-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6e62-153"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c6e62-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e62-154">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c6e62-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6e62-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c6e62-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c6e62-156">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c6e62-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c6e62-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6e62-157">See Also</span></span>

[<span data-ttu-id="c6e62-158">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="c6e62-158">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="c6e62-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c6e62-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c6e62-160">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="c6e62-160">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="c6e62-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c6e62-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c6e62-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c6e62-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c6e62-163">Jetregistercallback</span><span class="sxs-lookup"><span data-stu-id="c6e62-163">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="c6e62-164">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="c6e62-164">JetStopService</span></span>](./jetstopservice-function.md)
