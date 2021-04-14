---
description: 'Weitere Informationen finden Sie hier: JetInit3-Funktion'
title: JetInit3-Funktion
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350419"
---
# <a name="jetinit3-function"></a><span data-ttu-id="e9dc6-103">JetInit3-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9dc6-103">JetInit3 Function</span></span>


<span data-ttu-id="e9dc6-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9dc6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="e9dc6-105">JetInit3-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9dc6-105">JetInit3 Function</span></span>

<span data-ttu-id="e9dc6-106">Die **JetInit3** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="e9dc6-107">Die Engine muss bereits ordnungsgemäß für die Initialisierung konfiguriert sein, die Sie mithilfe der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="e9dc6-108">Beachten Sie, dass die Wiederherstellung von Daten Bank abstürzen automatisch als Teil des Initialisierungs Prozesses erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="e9dc6-109">**Windows Vista:**  **JetInit3** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e9dc6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9dc6-110">Parameters</span></span>

<span data-ttu-id="e9dc6-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="e9dc6-111">*pinstance*</span></span>

<span data-ttu-id="e9dc6-112">Die-Instanz, die Sie für einen bestimmten-Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="e9dc6-113">Die Verwendung dieses Parameters hängt vom Betriebsmodus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="e9dc6-114">Wenn die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) betrieben wird, in dem nur eine Instanz unterstützt wird, können Sie diesen Parameter entweder auf **null** oder auf einen gültigen Ausgabepuffer festlegen, der entweder **null** oder JET_instanceNil enthält, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="e9dc6-115">Dieser Instanzhandle kann dann an jede andere API weitergegeben werden, die eine-Instanz annimmt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="e9dc6-116">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, müssen Sie diesen Parameter auf einen gültigen Eingabepuffer festlegen, der das Instanzhandle enthält, das von der zu initialisierenden [jetkreateinstance](./jetcreateinstance-function.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="e9dc6-117">*prstinfo*</span><span class="sxs-lookup"><span data-stu-id="e9dc6-117">*prstInfo*</span></span>

<span data-ttu-id="e9dc6-118">Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zum Festlegen der Position, an der die Wiederherstellung beendet wird, oder zum Ermitteln des aktuellen Wiederherstellungs Status.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="e9dc6-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e9dc6-119">*grbit*</span></span>

<span data-ttu-id="e9dc6-120">Eine Gruppe von Bits, die NULL oder mehr Optionen angibt, die in der folgenden Tabelle aufgelistet und definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9dc6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e9dc6-121">Value</span></span></p></th>
<th><p><span data-ttu-id="e9dc6-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9dc6-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="e9dc6-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-124">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="e9dc6-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-126">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="e9dc6-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-128">Mit diesem Wert kann der Benutzer die Wiederherstellung für einen Satz von Protokolldateien ausführen, auch wenn keine Datenbanken vorhanden sind, die zu einem bestimmten Zeitpunkt an den Protokolldatei Satz angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="e9dc6-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-130">Mit diesem Wert kann der Benutzer die Wiederherstellung durchführen, aber nur bis zu (und nicht einschließlich) der Roll Back Phase.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="e9dc6-131">Mithilfe dieses Werts können zusätzliche Transaktionsprotokolle in kopiert und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="e9dc6-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-133">Dieser Wert bewirkt, dass Protokolldateien während einer erfolgreichen Soft-Wiederherstellung abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="e9dc6-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-135">Dieser Wert bewirkt, dass ein fehlender Daten Bank Zuordnungs Eintrag dem gleichen Speicherort entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="e9dc6-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-137">Dieser Wert bewirkt, dass Protokolle, die vom Ende des Protokolldaten Stroms verloren gehen, während einer Wiederherstellung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="e9dc6-138"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e9dc6-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9dc6-139">Return Value</span></span>

<span data-ttu-id="e9dc6-140">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="e9dc6-141">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e9dc6-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="e9dc6-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9dc6-142">Remarks</span></span>

<span data-ttu-id="e9dc6-143">Eine Instanz muss mit einem Aufrufen der **JetInit3** -Funktion initialisiert werden, bevor Sie von einem anderen als der [jetsetsystemparameter](./jetsetsystemparameter-function.md) -Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="e9dc6-144">Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mithilfe der [jetinit](./jetinit-function.md) -Funktion initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="e9dc6-145">Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="e9dc6-146">Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="e9dc6-147">Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="e9dc6-148">Beachten Sie, dass [jetterm](./jetterm-function.md) nicht aufgerufen werden sollte, wenn die **JetInit3** -Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="e9dc6-149">[Jetterm](./jetterm-function.md) sollte jedoch immer noch für alle Instanzen aufgerufen werden, die von **JetCreateInstance2** erstellt wurden, wenn **JetInit3** nie aufgerufen wurde oder **JetInit3** erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="e9dc6-150">Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle zugehörigen Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client möchte, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, wird der JET_bitReplayIgnoreMissingDB Fehler verwendet, um die Wiederherstellung für die verfügbaren Datenbanken fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="e9dc6-151">Da die Absturz Wiederherstellung in der Regel nicht auf dem gleichen Computer (und mit derselben Konfiguration) wie zum Zeitpunkt des Absturzes stattfindet, ändert sich eine Datenbank in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="e9dc6-152">In bestimmten Szenarien, z. b. beim Verschieben von Dateien auf einen anderen Computer oder beim Wiederherstellen der Momentaufnahme Sicherung an verschiedenen Speicherorten, ist dies nicht mehr der Fall</span><span class="sxs-lookup"><span data-stu-id="e9dc6-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="e9dc6-153">Mit der **JetInit3** -Funktion können Sie eine Zuordnung (mithilfe der [JET_RSTINFO](./jet-rstinfo-structure.md) -und [JET_RSTMAP](./jet-rstmap-structure.md) Strukturen) zwischen dem alten Daten Bank Speicherort und dem neuen Speicherort angeben.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="e9dc6-154">Tatsächlich benötigen Sie nur den neuen Speicherort, sofern die Datenbankdateien an diesem Speicherort vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="e9dc6-155">Sobald Sie die Speicherorte der wiederhergestellten Datenbanken kennen, wird die Daten Bank Signatur verwendet, um die Datenbank durch den Wiederherstellungs Vorgang zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="e9dc6-156">Sie benötigen den ursprünglichen Speicherort der Datenbank nur dann, wenn Sie eine Datenbank neu erstellen müssen. in diesem Fall ist die Signatur bekannt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="e9dc6-157">Wenn Sie eine Wiederherstellung nach einem Rückgängig-Vorgang beenden müssen, können Sie außerdem eine bestimmte Protokoll Position angeben, an der die Wiederherstellung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="e9dc6-158">Beachten Sie, dass die Möglichkeit besteht, am Ende einer bestimmten Protokoll Generierung anzuhalten, wenn die angegebene Position Teil der Generierung ist, aber hinter dem Ende des eigentlichen Protokolls liegt.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="e9dc6-159">Weitere Informationen finden Sie im Abschnitt "Hinweise" des Themas [jetinit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e9dc6-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e9dc6-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9dc6-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-161">Client</span><span class="sxs-lookup"><span data-stu-id="e9dc6-161">Client</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-162">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-163">Server</span><span class="sxs-lookup"><span data-stu-id="e9dc6-163">Server</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-164">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-165">Header</span><span class="sxs-lookup"><span data-stu-id="e9dc6-165">Header</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-166">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-167">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9dc6-167">Library</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-168">Verwendet ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9dc6-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e9dc6-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-170">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e9dc6-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9dc6-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="e9dc6-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="e9dc6-172">Implementiert als <strong>JetInit3W</strong> (Unicode) und <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e9dc6-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e9dc6-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9dc6-173">See Also</span></span>

[<span data-ttu-id="e9dc6-174">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="e9dc6-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="e9dc6-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e9dc6-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e9dc6-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e9dc6-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e9dc6-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e9dc6-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e9dc6-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="e9dc6-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="e9dc6-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="e9dc6-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="e9dc6-180">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="e9dc6-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e9dc6-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="e9dc6-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="e9dc6-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="e9dc6-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="e9dc6-183">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="e9dc6-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e9dc6-184">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="e9dc6-184">Resource Parameters</span></span>](./resource-parameters.md)
