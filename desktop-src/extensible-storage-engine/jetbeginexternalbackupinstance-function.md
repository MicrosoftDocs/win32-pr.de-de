---
description: Weitere Informationen finden Sie in der jetbeginexternalbackupinstance-Funktion.
title: Jetbeginexternalbackupinstance-Funktion
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484243"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="d4c4c-103">Jetbeginexternalbackupinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4c4c-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="d4c4c-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d4c4c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="d4c4c-105">Jetbeginexternalbackupinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4c4c-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="d4c4c-106">Die **jetbeginexternalbackupinstance** -Funktion initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="d4c4c-107">**Windows XP: jetbeginexternalbackupinstance** wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d4c4c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4c4c-108">Parameters</span></span>

<span data-ttu-id="d4c4c-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="d4c4c-109">*instance*</span></span>

<span data-ttu-id="d4c4c-110">Die Daten Bank Instanz, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-110">The database instance to use for this call.</span></span>

<span data-ttu-id="d4c4c-111">Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="d4c4c-112">In diesem Fall wird die Verwendung dieser globalen Instanz impliziert.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="d4c4c-113">Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="d4c4c-114">Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="d4c4c-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d4c4c-115">*grbit*</span></span>

<span data-ttu-id="d4c4c-116">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4c4c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c4c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="d4c4c-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d4c4c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4c4c-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="d4c4c-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="d4c4c-120">Dieses Flag ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-120">This flag is deprecated.</span></span> <span data-ttu-id="d4c4c-121">Die Verwendung dieses Bits führt dazu, dass JET_errInvalidgrbit zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4c4c-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="d4c4c-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="d4c4c-123">Erstellt im Gegensatz zu einer vollständigen Sicherung eine inkrementelle Sicherung.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="d4c4c-124">Dies bedeutet, dass nur die Protokolldateien seit der letzten vollständigen oder inkrementellen Sicherung gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4c4c-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4c4c-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="d4c4c-126">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-126">Reserved for future use.</span></span> <span data-ttu-id="d4c4c-127">Definiert für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d4c4c-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4c4c-128">Return Value</span></span>

<span data-ttu-id="d4c4c-129">Das System generiert möglicherweise Erfolgs-oder Fehlercodes, wenn diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="d4c4c-130">Eine umfassende Liste der Fehler für diese API finden Sie unter [Fehler Codes für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4c4c-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="d4c4c-131">Siehe [jetbeginexternalbackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4c4c-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="d4c4c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c4c-132">Remarks</span></span>

<span data-ttu-id="d4c4c-133">**Jetbeginexternalbackupinstance** ist die erste Funktion in einer Reihe von Funktionen, die aufgerufen werden müssen, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="d4c4c-134">Siehe auch [jetbeginexternalbackup](./jetbeginexternalbackup-function.md) und [jetstopbackupinstance](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4c4c-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="d4c4c-135">Eine externe Sicherung kann zum Implementieren von vollständigen, inkrementellen oder differenziellen Sicherungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="d4c4c-136">Bei der Sicherung handelt es sich um einen fuzzywert, da die Sicherung zu einem bestimmten Zeitpunkt im Transaktionsverlauf konsistent ist, aber das Steuern des genauen Zeitpunkts ist zurzeit nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d4c4c-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c4c-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4c4c-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d4c4c-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c4c-139">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4c4c-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d4c4c-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c4c-141">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4c4c-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d4c4c-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c4c-143">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4c4c-144"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d4c4c-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c4c-145">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4c4c-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d4c4c-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c4c-147">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d4c4c-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d4c4c-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4c4c-148">See Also</span></span>

[<span data-ttu-id="d4c4c-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d4c4c-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d4c4c-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d4c4c-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d4c4c-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d4c4c-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="d4c4c-152">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="d4c4c-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="d4c4c-153">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="d4c4c-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="d4c4c-154">Jetclosefile</span><span class="sxs-lookup"><span data-stu-id="d4c4c-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="d4c4c-155">Jetendexternalbackup</span><span class="sxs-lookup"><span data-stu-id="d4c4c-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="d4c4c-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="d4c4c-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="d4c4c-157">Jetgetattachinfo</span><span class="sxs-lookup"><span data-stu-id="d4c4c-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="d4c4c-158">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="d4c4c-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="d4c4c-159">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="d4c4c-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="d4c4c-160">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="d4c4c-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="d4c4c-161">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="d4c4c-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="d4c4c-162">Jettruneurelog</span><span class="sxs-lookup"><span data-stu-id="d4c4c-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
