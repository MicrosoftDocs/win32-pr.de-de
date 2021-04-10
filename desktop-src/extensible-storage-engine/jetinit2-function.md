---
description: 'Weitere Informationen finden Sie hier: JetInit2-Funktion'
title: JetInit2-Funktion
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961788"
---
# <a name="jetinit2-function"></a><span data-ttu-id="9369d-103">JetInit2-Funktion</span><span class="sxs-lookup"><span data-stu-id="9369d-103">JetInit2 Function</span></span>


<span data-ttu-id="9369d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9369d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="9369d-105">JetInit2-Funktion</span><span class="sxs-lookup"><span data-stu-id="9369d-105">JetInit2 Function</span></span>

<span data-ttu-id="9369d-106">Die **JetInit2** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="9369d-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="9369d-107">Die Engine muss für die Initialisierung mit [jetsetsystemparameter](./jetsetsystemparameter-function.md)bereits ordnungsgemäß konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="9369d-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="9369d-108">Die Daten Bank Absturz Wiederherstellung wird automatisch als Teil des Initialisierungs Prozesses ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9369d-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="9369d-109">**Windows XP:**  **JetInit2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9369d-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="9369d-110">Diese Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9369d-110">This function is obsolete.</span></span> <span data-ttu-id="9369d-111">Verwenden Sie stattdessen [JetInit3](./jetinit3-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9369d-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="9369d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9369d-112">Parameters</span></span>

<span data-ttu-id="9369d-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="9369d-113">*pinstance*</span></span>

<span data-ttu-id="9369d-114">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9369d-114">The instance to use for this call.</span></span>

<span data-ttu-id="9369d-115">Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9369d-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="9369d-116">Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="9369d-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="9369d-117">Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird, in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der NULL oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9369d-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="9369d-118">Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt.</span><span class="sxs-lookup"><span data-stu-id="9369d-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="9369d-119">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das von der zu initialisierende [jetkreateinstance](./jetcreateinstance-function.md) zurückgegebene Instanzhandle enthält.</span><span class="sxs-lookup"><span data-stu-id="9369d-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="9369d-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9369d-120">*grbit*</span></span>

<span data-ttu-id="9369d-121">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="9369d-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9369d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9369d-122">Value</span></span></p></th>
<th><p><span data-ttu-id="9369d-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9369d-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9369d-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="9369d-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="9369d-125">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9369d-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9369d-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="9369d-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="9369d-127">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9369d-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9369d-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="9369d-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="9369d-129">Mit dieser Option kann der Benutzer die Wiederherstellung für einen Satz von Protokolldateien ausführen, ohne dass alle Datenbanken vorhanden sind, die an einem Punkt des Protokoll Satzes angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9369d-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9369d-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="9369d-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="9369d-131">Führen Sie die Wiederherstellung aus, aber stoppen Sie die Roll Back Phase.</span><span class="sxs-lookup"><span data-stu-id="9369d-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="9369d-132">Dadurch können zusätzliche Transaktionsprotokolle in kopiert und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9369d-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9369d-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="9369d-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="9369d-134">Bei erfolgreicher Soft-Wiederherstellung kürzen Sie die Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="9369d-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9369d-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="9369d-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="9369d-136">Fehlender Daten Bank Zuordnungs Eintrag ist standardmäßig derselbe Speicherort.</span><span class="sxs-lookup"><span data-stu-id="9369d-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9369d-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="9369d-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="9369d-138">Ignorieren Sie die Protokolle, die am Ende des Protokolldaten Stroms verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="9369d-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="9369d-139"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9369d-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9369d-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9369d-140">Return Value</span></span>

<span data-ttu-id="9369d-141">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="9369d-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9369d-142">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9369d-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="9369d-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9369d-143">Remarks</span></span>

<span data-ttu-id="9369d-144">Eine Instanz muss mit einem **JetInit2** -Aufrufvorgang initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9369d-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="9369d-145">Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit [jetinit](./jetinit-function.md)initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9369d-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="9369d-146">Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="9369d-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="9369d-147">Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="9369d-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="9369d-148">Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="9369d-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="9369d-149">Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client wünscht, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, wird die JET_ bitreplayignoremissingdb verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="9369d-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="9369d-150">Weitere Informationen finden Sie im Abschnitt "Hinweise" in [jetinit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9369d-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9369d-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9369d-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9369d-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9369d-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9369d-153">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9369d-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9369d-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9369d-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9369d-155">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9369d-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9369d-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9369d-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9369d-157">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="9369d-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9369d-158"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="9369d-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9369d-159">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9369d-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9369d-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9369d-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9369d-161">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9369d-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9369d-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9369d-162">See Also</span></span>

[<span data-ttu-id="9369d-163">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="9369d-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="9369d-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9369d-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9369d-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9369d-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9369d-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9369d-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9369d-167">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="9369d-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="9369d-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="9369d-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="9369d-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="9369d-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="9369d-170">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="9369d-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9369d-171">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="9369d-171">Resource Parameters</span></span>](./resource-parameters.md)
