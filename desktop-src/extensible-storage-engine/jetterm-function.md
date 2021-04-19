---
description: 'Weitere Informationen zu: jetterm-Funktion'
title: JetTerm-Funktion
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346284"
---
# <a name="jetterm-function"></a><span data-ttu-id="c59b8-103">JetTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="c59b8-103">JetTerm Function</span></span>


<span data-ttu-id="c59b8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c59b8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="c59b8-105">JetTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="c59b8-105">JetTerm Function</span></span>

<span data-ttu-id="c59b8-106">Die **jetterm** -Funktion initiiert das Herunterfahren einer Instanz, die von [jetinit](./jetinit-function.md)initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c59b8-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="c59b8-107">**Jetterm** kann auch verwendet werden, um eine nicht initialisierte Instanz zu zerstören, die von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c59b8-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="c59b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c59b8-108">Parameters</span></span>

<span data-ttu-id="c59b8-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="c59b8-109">*instance*</span></span>

<span data-ttu-id="c59b8-110">Gibt die-Instanz an, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c59b8-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="c59b8-111">**Windows 2000:**  Dieser Parameter wird ignoriert und sollte immer **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c59b8-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="c59b8-112">**Versionen von Windows XP und höher:**  Dieser Parameter ist überladen.</span><span class="sxs-lookup"><span data-stu-id="c59b8-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="c59b8-113">Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) betrieben wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c59b8-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c59b8-114">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter ein Zeiger auf eine Instanz sein, die mithilfe von [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c59b8-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="c59b8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c59b8-115">Return Value</span></span>

<span data-ttu-id="c59b8-116">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c59b8-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c59b8-117">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c59b8-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c59b8-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c59b8-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c59b8-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c59b8-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c59b8-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c59b8-121">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c59b8-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c59b8-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c59b8-123">Einer der Parameter, die bereitgestellt wurden, enthielt einen unerwarteten Wert, oder die Kombination aus mehreren Parametern hat ein unerwartetes Ergebnis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c59b8-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="c59b8-124">Dieser Fehler wird von <strong>jetterm</strong> zurückgegeben, wenn sich die Engine im Modus für mehrere Instanzen befindet und <em>pinstance</em> auf eine ungültige Instanz verweist.</span><span class="sxs-lookup"><span data-stu-id="c59b8-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="c59b8-125"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c59b8-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c59b8-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c59b8-127">Der Vorgang kann nicht abgeschlossen werden, da die Instanz noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c59b8-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c59b8-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c59b8-129">Der Vorgang kann nicht ausgeführt werden, da die Instanz heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c59b8-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c59b8-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c59b8-131">Der Vorgang kann nicht abgeschlossen werden, da für die Instanz ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c59b8-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="c59b8-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="c59b8-133">Der Vorgang kann nicht abgeschlossen werden, da für die Instanz zurzeit ein Sicherungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c59b8-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="c59b8-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="c59b8-135">Die Instanz kann nicht heruntergefahren werden, da derzeit Sitzungen mit aktiven Transaktionen für die angegebene Instanz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c59b8-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="c59b8-136">Dieser Fehler tritt nur auf, wenn die JET_bitTermComplete verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c59b8-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c59b8-137">Wenn diese Funktion erfolgreich ausgeführt wird, wird die angegebene Instanz heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="c59b8-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="c59b8-138">Der Instanzhandle wird auch geschlossen und für jede API, die einen Instanzhandle annimmt, nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="c59b8-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="c59b8-139">Alle anderen Objekte, die der-Instanz zugeordnet sind, z. b. Sitzungen, werden ebenfalls geschlossen.</span><span class="sxs-lookup"><span data-stu-id="c59b8-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="c59b8-140">Der Status der Prüf Punkt Datei, der Transaktionsprotokoll Dateien und der Datenbankdateien, die an die Instanz angefügt sind, werden während des Beendigungs Vorgangs geändert.</span><span class="sxs-lookup"><span data-stu-id="c59b8-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="c59b8-141">Wenn diese Funktion aufgrund eines Verwendungs Fehlers nicht ausgeführt werden kann, verbleibt die Instanz in einem initialisierten Zustand, und es werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="c59b8-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="c59b8-142">Andernfalls wird die Instanz weiterhin gemäß dem Erfolgsfall heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="c59b8-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="c59b8-143">Der Unterschied besteht darin, dass die Instanz bei der nächsten Initialisierung die Wiederherstellung von Abstürzen durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="c59b8-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="c59b8-144">Die Engine versucht, so viele Daten wie möglich zu leeren, um die erforderliche Wiederherstellungs Menge zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="c59b8-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="c59b8-145">Konzeptionell ist ein solcher Ausfall von **jetterm** nicht anders als bei einem Prozess Absturz.</span><span class="sxs-lookup"><span data-stu-id="c59b8-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c59b8-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59b8-146">Remarks</span></span>

<span data-ttu-id="c59b8-147">Wenn der Host Prozess einer Instanz aus einem beliebigen Grund vor **jetterm** erfolgreich für diese Instanz aufgerufen wird, wird die Instanz als abgestürzt eingestuft.</span><span class="sxs-lookup"><span data-stu-id="c59b8-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="c59b8-148">Beim nächsten Versuch, diese Instanz zu initialisieren, erfolgt die Wiederherstellung von Abstürzen.</span><span class="sxs-lookup"><span data-stu-id="c59b8-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c59b8-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c59b8-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c59b8-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c59b8-151">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c59b8-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c59b8-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c59b8-153">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c59b8-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-154"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c59b8-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c59b8-155">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c59b8-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c59b8-156"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c59b8-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c59b8-157">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c59b8-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c59b8-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c59b8-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c59b8-159">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c59b8-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c59b8-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c59b8-160">See Also</span></span>

[<span data-ttu-id="c59b8-161">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="c59b8-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="c59b8-162">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="c59b8-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c59b8-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c59b8-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c59b8-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c59b8-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c59b8-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="c59b8-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c59b8-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c59b8-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c59b8-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="c59b8-167">JetTerm2</span></span>](./jetterm2-function.md)
