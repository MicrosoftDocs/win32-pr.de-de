---
description: 'Weitere Informationen finden Sie hier: JetTerm2-Funktion'
title: JetTerm2-Funktion
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129717"
---
# <a name="jetterm2-function"></a><span data-ttu-id="a6d62-103">JetTerm2-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6d62-103">JetTerm2 Function</span></span>


<span data-ttu-id="a6d62-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a6d62-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="a6d62-105">JetTerm2-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6d62-105">JetTerm2 Function</span></span>

<span data-ttu-id="a6d62-106">Die **JetTerm2** -Funktion initiiert das Herunterfahren einer Instanz, die von [jetinit](./jetinit-function.md)initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a6d62-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="a6d62-107">**JetTerm2** kann auch eine nicht initialisierte Instanz zerstören, die von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a6d62-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a6d62-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6d62-108">Parameters</span></span>

<span data-ttu-id="a6d62-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="a6d62-109">*instance*</span></span>

<span data-ttu-id="a6d62-110">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6d62-110">The instance to use for this call.</span></span>

<span data-ttu-id="a6d62-111">**Windows 2000:**  Dieser Parameter wird ignoriert und sollte immer **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a6d62-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="a6d62-112">**Versionen von Windows XP und höher:**  Dieser Parameter ist überladen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="a6d62-113">Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) betrieben wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="a6d62-114">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter ein Zeiger auf eine Instanz sein, die mithilfe von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a6d62-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="a6d62-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a6d62-115">*grbit*</span></span>

<span data-ttu-id="a6d62-116">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6d62-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6d62-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a6d62-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a6d62-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a6d62-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="a6d62-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="a6d62-120">Fordert an, dass die Instanz ordnungsgemäß heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="a6d62-121">Alle optionalen Bereinigungs arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden sofort abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="a6d62-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="a6d62-123">Fordert an, dass die Instanz so schnell wie möglich heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="a6d62-124">Alle optionalen arbeiten, die normalerweise zur Laufzeit im Hintergrund durchgeführt werden, werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="a6d62-125"><strong>Hinweis</strong>  Diese Option kann zum Verlust vorübergehender oder dauerhafter Speicherplatz in der Datenbank führen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="a6d62-126">Dieser verlorene Speicherplatz kann immer durch eine Offline Defragmentierung der Datenbank wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6d62-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="a6d62-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="a6d62-128">Fordert an, dass die Instanz heruntergefahren wird, auch wenn zurzeit eine Sicherung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="a6d62-129">Normalerweise bewirkt eine ausstehende Sicherung, dass <a href="gg269298(v=exchg.10).md">jetterm</a> mit JET_errBackupInProgress fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a6d62-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="a6d62-130">Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert JET_bitTermAbrupt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="a6d62-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="a6d62-132">Fordert an, dass die Instanz mit allen angefügten Datenbanken heruntergefahren wird, die in einem fehlerhaften Zustand bleiben.</span><span class="sxs-lookup"><span data-stu-id="a6d62-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="a6d62-133">Windows 7: JET_bitTermDirty wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a6d62-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a6d62-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6d62-134">Return Value</span></span>

<span data-ttu-id="a6d62-135">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a6d62-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a6d62-136">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6d62-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6d62-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a6d62-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="a6d62-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6d62-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a6d62-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a6d62-140">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="a6d62-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="a6d62-142">Der Vorgang kann nicht abgeschlossen werden, da für die Instanz zurzeit ein Sicherungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a6d62-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a6d62-144">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6d62-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="a6d62-145">Dieser Fehler wird von <a href="gg269298(v=exchg.10).md">jetterm</a> zurückgegeben, wenn sich die Engine im Modus für mehrere Instanzen befindet und <em>pinstance</em> auf eine ungültige Instanz verweist.</span><span class="sxs-lookup"><span data-stu-id="a6d62-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="a6d62-146"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a6d62-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a6d62-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a6d62-148">Der Vorgang kann nicht abgeschlossen werden, da die Instanz noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a6d62-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a6d62-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a6d62-150">Der Vorgang kann nicht ausgeführt werden, da die Instanz heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a6d62-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a6d62-152">Der Vorgang kann nicht abgeschlossen werden, da für die Instanz ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="a6d62-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="a6d62-154">Die Instanz kann nicht heruntergefahren werden, da derzeit Sitzungen mit aktiven Transaktionen für die angegebene Instanz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a6d62-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="a6d62-155">Dieser Fehler tritt nur auf, wenn die JET_bitTermComplete verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6d62-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a6d62-156">Wenn diese Funktion erfolgreich ausgeführt wird, wird die angegebene Instanz heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="a6d62-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="a6d62-157">Der Instanzhandle wird auch geschlossen und für jede API, die einen Instanzhandle annimmt, nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a6d62-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="a6d62-158">Alle anderen Objekte, die der-Instanz zugeordnet sind, z. b. Sitzungen, werden ebenfalls geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="a6d62-159">Der Status der Prüf Punkt Datei, der Transaktionsprotokoll Dateien und der Datenbankdateien, die an die Instanz angefügt sind, werden während des Beendigungs Vorgangs geändert.</span><span class="sxs-lookup"><span data-stu-id="a6d62-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="a6d62-160">Wenn diese Funktion aufgrund eines Verwendungs Fehlers fehlschlägt, verbleibt die Instanz in einem initialisierten Zustand, und es werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a6d62-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="a6d62-161">Andernfalls wird die Instanz nach wie vor für den Erfolgsfall heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="a6d62-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="a6d62-162">Der Unterschied besteht darin, dass die Instanz bei der nächsten Initialisierung die Wiederherstellung von Abstürzen durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="a6d62-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="a6d62-163">Die Engine versucht, so viele Daten wie möglich zu leeren, um die erforderliche Wiederherstellungs Menge zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="a6d62-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="a6d62-164">Konzeptionell ist ein solcher Ausfall von [jetterm](./jetterm-function.md) nicht anders als bei einem Prozess Absturz.</span><span class="sxs-lookup"><span data-stu-id="a6d62-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a6d62-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6d62-165">Remarks</span></span>

<span data-ttu-id="a6d62-166">Siehe [jetterm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="a6d62-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="a6d62-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6d62-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a6d62-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d62-169">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a6d62-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a6d62-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d62-171">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a6d62-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a6d62-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d62-173">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a6d62-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d62-174"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a6d62-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d62-175">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a6d62-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6d62-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a6d62-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d62-177">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a6d62-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a6d62-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6d62-178">See Also</span></span>

[<span data-ttu-id="a6d62-179">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="a6d62-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="a6d62-180">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="a6d62-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a6d62-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a6d62-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a6d62-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a6d62-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a6d62-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="a6d62-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="a6d62-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a6d62-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a6d62-185">Jetterm</span><span class="sxs-lookup"><span data-stu-id="a6d62-185">JetTerm</span></span>](./jetterm-function.md)
