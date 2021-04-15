---
description: 'Weitere Informationen zu: jetclosefilinput Stance-Funktion'
title: Jetclosefilinput Stance-Funktion
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524968"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="99ff4-103">Jetclosefilinput Stance-Funktion</span><span class="sxs-lookup"><span data-stu-id="99ff4-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="99ff4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="99ff4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="99ff4-105">Jetclosefilinput Stance-Funktion</span><span class="sxs-lookup"><span data-stu-id="99ff4-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="99ff4-106">Die **jetclosefileinstance** -Funktion schließt eine Datei, die mit [jetopenfileinstance](./jetopenfileinstance-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [jetreadfileinstance](./jetreadfileinstance-function.md)extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="99ff4-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="99ff4-107">**Windows XP: jetclosefileinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99ff4-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="99ff4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99ff4-108">Parameters</span></span>

<span data-ttu-id="99ff4-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="99ff4-109">*instance*</span></span>

<span data-ttu-id="99ff4-110">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99ff4-110">The instance to use for this call.</span></span>

<span data-ttu-id="99ff4-111">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="99ff4-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="99ff4-112">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="99ff4-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="99ff4-113">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="99ff4-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="99ff4-114">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="99ff4-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="99ff4-115">*hffile*</span><span class="sxs-lookup"><span data-stu-id="99ff4-115">*hfFile*</span></span>

<span data-ttu-id="99ff4-116">Das Handle der zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="99ff4-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="99ff4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99ff4-117">Return Value</span></span>

<span data-ttu-id="99ff4-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="99ff4-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="99ff4-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="99ff4-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="99ff4-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="99ff4-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="99ff4-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ff4-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="99ff4-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="99ff4-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="99ff4-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="99ff4-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="99ff4-125">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg294108(v=exchg.10).md">jetstopserviceinstance</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="99ff4-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="99ff4-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="99ff4-127">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="99ff4-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="99ff4-128">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99ff4-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="99ff4-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="99ff4-130">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99ff4-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="99ff4-131">Dies kann bei <strong>jetclosefilinput Stance</strong> vorkommen, wenn:</span><span class="sxs-lookup"><span data-stu-id="99ff4-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="99ff4-132">Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="99ff4-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="99ff4-133">Das angegebene Datei Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="99ff4-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="99ff4-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="99ff4-135">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99ff4-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="99ff4-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="99ff4-137">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="99ff4-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="99ff4-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="99ff4-139">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99ff4-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="99ff4-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="99ff4-141">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="99ff4-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="99ff4-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="99ff4-143">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="99ff4-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="99ff4-144">Bei Erfolg wird das Datei Handle geschlossen.</span><span class="sxs-lookup"><span data-stu-id="99ff4-144">On success, the file handle is closed.</span></span> <span data-ttu-id="99ff4-145">Wenn eine Datenbankdatei geschlossen wurde, wird die zugehörige datenbankpatchdatei (falls vorhanden) zerstört.</span><span class="sxs-lookup"><span data-stu-id="99ff4-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="99ff4-146">Bei einem Fehler erfolgt keine Änderung.</span><span class="sxs-lookup"><span data-stu-id="99ff4-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="99ff4-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99ff4-147">Remarks</span></span>

<span data-ttu-id="99ff4-148">Die Datenbank-Engine unterstützt zurzeit nur eine geöffnete Datei durch [jetopenfileinstance](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="99ff4-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="99ff4-149">Wenn ein Datei Handle mit [jetopenfileinstance](./jetopenfileinstance-function.md) geöffnet wird, muss es mithilfe von **jetclosefileinstance** geschlossen werden, bevor eine andere Datei geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="99ff4-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="99ff4-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99ff4-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="99ff4-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="99ff4-152">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="99ff4-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="99ff4-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="99ff4-154">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="99ff4-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="99ff4-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="99ff4-156">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="99ff4-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="99ff4-157"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="99ff4-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="99ff4-158">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="99ff4-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="99ff4-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="99ff4-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="99ff4-160">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="99ff4-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="99ff4-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99ff4-161">See Also</span></span>

[<span data-ttu-id="99ff4-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="99ff4-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="99ff4-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="99ff4-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="99ff4-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="99ff4-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="99ff4-165">Jetopeinfileinstance</span><span class="sxs-lookup"><span data-stu-id="99ff4-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="99ff4-166">Jetreadfilinput Stance</span><span class="sxs-lookup"><span data-stu-id="99ff4-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="99ff4-167">Jetstopserviczustance</span><span class="sxs-lookup"><span data-stu-id="99ff4-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
