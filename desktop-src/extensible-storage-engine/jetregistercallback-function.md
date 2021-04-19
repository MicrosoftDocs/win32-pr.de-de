---
description: 'Weitere Informationen zu: jetregistercallback-Funktion'
title: JetRegisterCallback-Funktion
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ca7559488182f2d687d5c678639e108792f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348172"
---
# <a name="jetregistercallback-function"></a><span data-ttu-id="43969-103">JetRegisterCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="43969-103">JetRegisterCallback Function</span></span>


<span data-ttu-id="43969-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="43969-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetregistercallback-function"></a><span data-ttu-id="43969-105">JetRegisterCallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="43969-105">JetRegisterCallback Function</span></span>

<span data-ttu-id="43969-106">Die **jetregistercallback** -Funktion ermöglicht es der Anwendung, die Datenbank-Engine so zu konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43969-106">The **JetRegisterCallback** function allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="43969-107">Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von [jetterm](./jetterm-function.md)heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="43969-107">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="43969-108">**Windows XP: jetregistercallback** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="43969-108">**Windows XP:  JetRegisterCallback** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a><span data-ttu-id="43969-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43969-109">Parameters</span></span>

<span data-ttu-id="43969-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="43969-110">*sesid*</span></span>

<span data-ttu-id="43969-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43969-111">The session to use for this call.</span></span>

<span data-ttu-id="43969-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="43969-112">*tableid*</span></span>

<span data-ttu-id="43969-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43969-113">The cursor to use for this call.</span></span>

<span data-ttu-id="43969-114">*cbyp*</span><span class="sxs-lookup"><span data-stu-id="43969-114">*cbtyp*</span></span>

<span data-ttu-id="43969-115">Eine Bitmaske, die aus den Rückruf Gründen besteht, für die die Anwendung Benachrichtigungen empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="43969-115">A bit mask composed of the callback reasons for which the application wishes to receive notifications.</span></span>

<span data-ttu-id="43969-116">Um diese Bitmaske zu erstellen, führen Sie einfach oder zusammengültige Rückruf Gründe aus der [JET_CBTYP](./jet-cbtyp.md) Enumeration aus.</span><span class="sxs-lookup"><span data-stu-id="43969-116">To create this bit mask, simply or together valid callback reasons from the [JET_CBTYP](./jet-cbtyp.md) enumeration.</span></span>

<span data-ttu-id="43969-117">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="43969-117">*pCallback*</span></span>

<span data-ttu-id="43969-118">Der Funktionszeiger auf die Rückruffunktion für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="43969-118">The function pointer to the callback function for the application.</span></span>

<span data-ttu-id="43969-119">*pvcontext*</span><span class="sxs-lookup"><span data-stu-id="43969-119">*pvContext*</span></span>

<span data-ttu-id="43969-120">Gibt einen Kontext Zeiger an, der der Rückruffunktion für die Anwendung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="43969-120">Specifies a context pointer that will be given to the callback function for the application.</span></span>

<span data-ttu-id="43969-121">*phcallbackid*</span><span class="sxs-lookup"><span data-stu-id="43969-121">*phCallbackId*</span></span>

<span data-ttu-id="43969-122">Gibt ein Handle zurück, das später verwendet werden kann, um die Registrierung der angegebenen Rückruffunktion mit [jetunregistercallback](./jetunregistercallback-function.md)abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="43969-122">Returns a handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback](./jetunregistercallback-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="43969-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43969-123">Return Value</span></span>

<span data-ttu-id="43969-124">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="43969-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="43969-125">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="43969-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43969-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="43969-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="43969-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43969-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43969-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="43969-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="43969-129">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="43969-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="43969-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="43969-131">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="43969-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43969-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="43969-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="43969-133">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="43969-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="43969-134">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43969-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="43969-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="43969-136">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="43969-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="43969-137">Dieser Fehler wird von <strong>jetregistercallback</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="43969-137">This error will be returned by <strong>JetRegisterCallback</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="43969-138"><em>cbyp</em> ist 0 (null),</span><span class="sxs-lookup"><span data-stu-id="43969-138"><em>cbtyp</em> is zero,</span></span></p></li>
<li><p><span data-ttu-id="43969-139"><em>pCallback</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="43969-139"><em>pCallback</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="43969-140"><em>phcallbackid</em> ist NULL.</span><span class="sxs-lookup"><span data-stu-id="43969-140"><em>phCallbackId</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43969-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="43969-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="43969-142">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="43969-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="43969-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="43969-144">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43969-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43969-145">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="43969-145">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="43969-146">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43969-146">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="43969-147">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="43969-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-148">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="43969-148">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="43969-149">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="43969-149">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43969-150">Bei Erfolg wird der angegebene Rückruf für die angegebenen Rückruf Gründe mit der Tabelle, die dem angegebenen Cursor zugeordnet ist, registriert.</span><span class="sxs-lookup"><span data-stu-id="43969-150">On success, the specified callback will be registered for the given callback reasons with the table associated with the given cursor.</span></span> <span data-ttu-id="43969-151">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="43969-151">No change to the database state will occur.</span></span>

<span data-ttu-id="43969-152">Bei einem Fehler wird der Rückruf nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="43969-152">On failure, the callback will not be registered.</span></span> <span data-ttu-id="43969-153">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="43969-153">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="43969-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43969-154">Remarks</span></span>

<span data-ttu-id="43969-155">Diese Methode stellt eine Möglichkeit bereit, mit der die Anwendung flüchtige Rückrufe einer Tabelle in einer Datenbank zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="43969-155">This method provides a means for the application to associate volatile callbacks with a table in a database.</span></span> <span data-ttu-id="43969-156">Wenn die Anwendung persistente Rückrufe einer Tabelle in der Datenbank zuordnen möchte, sollte Sie den Rückruf an [JET_TABLECREATE](./jet-tablecreate-structure.md) mithilfe von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="43969-156">If the application wishes to associate persisted callbacks with a table in the database then it should pass the callback to [JET_TABLECREATE](./jet-tablecreate-structure.md) using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="43969-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43969-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43969-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="43969-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="43969-159">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="43969-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="43969-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="43969-161">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="43969-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43969-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="43969-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="43969-163">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="43969-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43969-164"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="43969-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="43969-165">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="43969-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43969-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="43969-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="43969-167">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="43969-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="43969-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43969-168">See Also</span></span>

[<span data-ttu-id="43969-169">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="43969-169">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="43969-170">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="43969-170">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="43969-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="43969-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="43969-172">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="43969-172">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="43969-173">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="43969-173">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="43969-174">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="43969-174">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="43969-175">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="43969-175">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="43969-176">Jetterm</span><span class="sxs-lookup"><span data-stu-id="43969-176">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="43969-177">Jetunregistercallback</span><span class="sxs-lookup"><span data-stu-id="43969-177">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)
