---
description: 'Weitere Informationen zu: jetclosefile-Funktion'
title: Jetclosefile-Funktion
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393381"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="a02ae-103">Jetclosefile-Funktion</span><span class="sxs-lookup"><span data-stu-id="a02ae-103">JetCloseFile Function</span></span>


<span data-ttu-id="a02ae-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a02ae-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="a02ae-105">Jetclosefile-Funktion</span><span class="sxs-lookup"><span data-stu-id="a02ae-105">JetCloseFile Function</span></span>

<span data-ttu-id="a02ae-106">Die **jetclosefile** -Funktion schließt eine Datei, die mit [jetopenfile](./jetopenfile-function.md) geöffnet wurde, nachdem die Daten aus dieser Datei mit [jetreadfile](./jetreadfile-function.md)extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a02ae-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="a02ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a02ae-107">Parameters</span></span>

<span data-ttu-id="a02ae-108">*hffile*</span><span class="sxs-lookup"><span data-stu-id="a02ae-108">*hfFile*</span></span>

<span data-ttu-id="a02ae-109">Das Handle der zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="a02ae-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="a02ae-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a02ae-110">Return Value</span></span>

<span data-ttu-id="a02ae-111">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a02ae-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a02ae-112">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a02ae-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a02ae-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a02ae-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="a02ae-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a02ae-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a02ae-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a02ae-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a02ae-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a02ae-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a02ae-118">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a02ae-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a02ae-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a02ae-120">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a02ae-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a02ae-121">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a02ae-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a02ae-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a02ae-123">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="a02ae-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a02ae-124">Dies kann bei <strong>jetclosefile</strong> vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="a02ae-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a02ae-125">Das angegebene Instanzhandle ist ungültig (Windows XP und spätere Releases),</span><span class="sxs-lookup"><span data-stu-id="a02ae-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="a02ae-126">Das angegebene Datei Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a02ae-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a02ae-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a02ae-128">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a02ae-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a02ae-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a02ae-130">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a02ae-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a02ae-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a02ae-132">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a02ae-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a02ae-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a02ae-134">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a02ae-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a02ae-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a02ae-136">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a02ae-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a02ae-137">Bei Erfolg wird das Datei Handle geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a02ae-137">On success, the file handle is closed.</span></span> <span data-ttu-id="a02ae-138">Wenn eine Datenbankdatei geschlossen wurde, wird die zugehörige datenbankpatchdatei (falls vorhanden) zerstört.</span><span class="sxs-lookup"><span data-stu-id="a02ae-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="a02ae-139">Bei einem Fehler erfolgt keine Änderung.</span><span class="sxs-lookup"><span data-stu-id="a02ae-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a02ae-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a02ae-140">Remarks</span></span>

<span data-ttu-id="a02ae-141">Die Datenbank-Engine unterstützt zurzeit nur eine geöffnete Datei durch [jetopenfile](./jetopenfile-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a02ae-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="a02ae-142">Wenn ein Datei Handle mit [jetopenfile](./jetopenfile-function.md) geöffnet wird, muss es mithilfe von **jetclosefile** geschlossen werden, bevor eine andere Datei geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a02ae-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a02ae-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a02ae-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a02ae-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a02ae-145">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a02ae-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a02ae-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a02ae-147">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a02ae-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a02ae-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a02ae-149">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a02ae-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a02ae-150"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a02ae-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a02ae-151">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a02ae-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a02ae-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a02ae-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a02ae-153">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a02ae-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a02ae-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a02ae-154">See Also</span></span>

[<span data-ttu-id="a02ae-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a02ae-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a02ae-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a02ae-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a02ae-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a02ae-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a02ae-158">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="a02ae-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="a02ae-159">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="a02ae-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="a02ae-160">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="a02ae-160">JetStopService</span></span>](./jetstopservice-function.md)
