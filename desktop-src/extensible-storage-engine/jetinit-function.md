---
description: 'Weitere Informationen zu: jetinit-Funktion'
title: JetInit-Funktion
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356216"
---
# <a name="jetinit-function"></a><span data-ttu-id="a016d-103">JetInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="a016d-103">JetInit Function</span></span>


<span data-ttu-id="a016d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a016d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="a016d-105">JetInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="a016d-105">JetInit Function</span></span>

<span data-ttu-id="a016d-106">Die **jetinit** -Funktion versetzt die Datenbank-Engine in einen Zustand, in dem Sie die Anwendungs Verwendung von Datenbankdateien unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a016d-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="a016d-107">Die Engine muss für die Initialisierung mit [jetsetsystemparameter](./jetsetsystemparameter-function.md)bereits ordnungsgemäß konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="a016d-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="a016d-108">Die Daten Bank Absturz Wiederherstellung wird automatisch als Teil des Initialisierungs Prozesses ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a016d-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="a016d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a016d-109">Parameters</span></span>

<span data-ttu-id="a016d-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="a016d-110">*pinstance*</span></span>

<span data-ttu-id="a016d-111">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a016d-111">The instance to use for this call.</span></span>

<span data-ttu-id="a016d-112">Für Windows 2000 wird dieser Parameter ignoriert und sollte immer NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a016d-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="a016d-113">Für Windows XP und spätere Versionen hängt die Verwendung dieses Parameters vom Betriebsmodus der Engine ab.</span><span class="sxs-lookup"><span data-stu-id="a016d-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="a016d-114">Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter entweder NULL sein, oder er kann auf einen gültigen Ausgabepuffer festgelegt werden, der das globale Instanzhandle zurückgibt, das als Nebeneffekt der Initialisierung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a016d-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="a016d-115">Dieser Ausgabepuffer muss auf NULL oder JET_instanceNil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a016d-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="a016d-116">Dieser Instanzhandle kann dann an jede andere Funktion weitergegeben werden, die eine-Instanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="a016d-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="a016d-117">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, muss dieser Parameter auf einen gültigen Eingabepuffer festgelegt werden, der das Instanzhandle enthält, das von der initialisierten [jetkreateinstance](./jetcreateinstance-function.md) -Funktions Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a016d-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="a016d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a016d-118">Remarks</span></span>

<span data-ttu-id="a016d-119">Eine Instanz muss mit einem **calltinit** -Namen initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a016d-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="a016d-120">Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit **jetinit** initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a016d-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="a016d-121">Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="a016d-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="a016d-122">Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="a016d-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="a016d-123">Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="a016d-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="a016d-124">Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, der durch einen Aufruf von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a016d-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="a016d-125">Wenn die Datenbank-Engine zum ersten Mal initialisiert wird, erstellt **jetinit** einen anfänglichen Satz von Dateien, um diese Instanz zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a016d-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="a016d-126">Diese Dateien enthalten eine Prüf Punkt Datei (mit dem Namen) \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), eine Reihe von reservierten Transaktionsprotokoll Dateien (mit dem Namen RES1. Log und RES2. Log), eine anfängliche Transaktionsprotokoll Datei (mit dem Namen) \<[JET_paramBaseName](./transaction-log-parameters.md)\> . Log) und eine temporäre Datenbankdatei (benannt nach [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="a016d-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="a016d-127">Wenn [JET_paramRecovery](./transaction-log-parameters.md) auf "Off" festgelegt ist, werden die Prüf Punkt Datei und die Protokolldateien nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="a016d-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="a016d-128">Wenn [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) auf NULL festgelegt ist, wird die temporäre Datenbankdatei nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="a016d-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="a016d-129">Diese Dateien stellen den Speicherbedarf einer Instanz auf einem Datenträger dar und müssen mit Bedacht verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a016d-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="a016d-130">Wenn diese Dateien einzeln oder in Bezug auf einen anderen beschädigt werden, gehen die Daten, die in den Datenbanken gespeichert sind, die der Instanz zugeordnet sind, möglicherweise verloren.</span><span class="sxs-lookup"><span data-stu-id="a016d-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="a016d-131">Wenn die Datenbank-Engine mit einem vorhandenen Satz von Transaktionsprotokoll Dateien initialisiert wird, werden diese Dateien überprüft, um festzustellen, ob die vorherige Inkarnation der Instanz durch einen Absturz verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="a016d-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="a016d-132">Wenn ein Absturz erkannt wird, wird automatisch die Wiederherstellung von Abstürzen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a016d-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="a016d-133">Bei diesem Vorgang werden die Datenbanken, die während der vorherigen Inkarnation der Engine an die Instanz angefügt sind, rekonstruiert und die Änderungen in den Datenbankdateien wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="a016d-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="a016d-134">Das Ergebnis sind Datenbanken, die Transaktions konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="a016d-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="a016d-135">Dieser Vorgang kann einige Zeit in Anspruch nehmen, wenn die Anzahl der Transaktionsprotokoll Dateien, die für die Datenbanken wiedergegeben werden sollen, sehr groß ist.</span><span class="sxs-lookup"><span data-stu-id="a016d-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="a016d-136">Aufgrund der Tatsache, dass **jetinit** die Wiederherstellung von Abstürzen ausführt, ist es möglich, dass im Falle eines Fehlers fast jeder Datenbank-Engine-Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a016d-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="a016d-137">In der Praxis werden die meisten Fehler in der Bereitstellung in zwei Kategorien unterteilt: Daten Beschädigung und Datei Misswirtschaft.</span><span class="sxs-lookup"><span data-stu-id="a016d-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="a016d-138">Daten Beschädigungen werden am häufigsten in den folgenden oder ähnlichen Fehlern angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a016d-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="a016d-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a016d-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="a016d-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="a016d-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="a016d-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="a016d-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="a016d-142">Diese Fehler werden fast immer durch Hardwareprobleme verursacht und können daher nicht vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="a016d-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="a016d-143">Die Datei Misswirtschaft wird am häufigsten in den folgenden oder ähnlichen Fehlern angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a016d-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="a016d-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="a016d-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="a016d-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="a016d-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="a016d-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a016d-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="a016d-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="a016d-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="a016d-148">Wenn die Wiederherstellung für eine Gruppe von Protokollen ausgeführt wird, für die nicht alle Datenbanken vorhanden sind (was den Fehler JET_errAttachedDatabaseMismatch unter normalen Umständen zurückgibt), und der Client wünscht, dass die Wiederherstellung trotz fehlender Datenbanken fortgesetzt wird, kann die JET_ bitreplayignoremissingdb verwendet werden, um die Wiederherstellung der verfügbaren Datenbanken fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a016d-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="a016d-149">Diese Fehler können von der Anwendung verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="a016d-149">These errors are preventable by the application.</span></span> <span data-ttu-id="a016d-150">Die Anwendung muss darauf achten, das Repository dieser Dateien vor der Bearbeitung durch externe Kräfte wie z. b. den Benutzer oder andere Anwendungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a016d-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="a016d-151">Wenn die Anwendung eine Instanz vollständig zerstören möchte, müssen alle Dateien, die der Instanz zugeordnet sind, gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a016d-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="a016d-152">Hierzu gehören die Prüf Punkt Datei, die Transaktionsprotokoll Dateien und alle Datenbankdateien, die an die Instanz angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="a016d-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="a016d-153">Die **jetinit** -Funktion verhält sich in Bezug auf die Datenbankdateien, die an die Instanz angefügt sind, zwischen Windows 2000 und neueren Versionen anders.</span><span class="sxs-lookup"><span data-stu-id="a016d-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="a016d-154">**Windows 2000:**  In Windows 2000 bleibt jede Datenbank, die während einer früheren Inkarnation dieser Instanz an die Instanz angefügt ist, nach der erfolgreichen Ausführung von **jetinit** an die Instanz angefügt.</span><span class="sxs-lookup"><span data-stu-id="a016d-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="a016d-155">Es ist nicht erforderlich, [jetattachdatabase](./jetattachdatabase-function.md) nach **jetinit** aufzurufen, um den späteren Datenbankzugriff zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="a016d-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="a016d-156">Wenn die [jetattachdatabase](./jetattachdatabase-function.md) -Funktion nach der **jetinit** -Funktion aufgerufen wird, wird die JET_wrnDatabaseAttached Warnung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a016d-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="a016d-157">Diese Warnung gibt an, dass die Daten Bank Anlage beibehalten wurde und ignoriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a016d-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="a016d-158">**Windows XP:**  In Windows XP und späteren Versionen werden alle Datenbanken von **jetinit** automatisch von der Instanz getrennt.</span><span class="sxs-lookup"><span data-stu-id="a016d-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="a016d-159">Dies bedeutet, dass [jetattachdatabase](./jetattachdatabase-function.md) in diesem Fall immer nach **jetinit** aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a016d-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="a016d-160">Jede Anwendung, die für die Ausführung unter Windows 2000 und späteren Versionen geschrieben wird, muss [jetattachdatabase](./jetattachdatabase-function.md) nach **jetinit** immer anrufen.</span><span class="sxs-lookup"><span data-stu-id="a016d-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="a016d-161">Wenn die Anwendung unter Windows 2000 ausgeführt wird, muss Sie in einigen Fällen JET_wrnDatabaseAttached erwarten.</span><span class="sxs-lookup"><span data-stu-id="a016d-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="a016d-162">Weitere Informationen finden Sie unter [jetattachdatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a016d-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a016d-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a016d-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a016d-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a016d-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a016d-165">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a016d-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a016d-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a016d-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a016d-167">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a016d-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a016d-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a016d-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a016d-169">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a016d-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a016d-170"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a016d-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a016d-171">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a016d-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a016d-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a016d-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a016d-173">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a016d-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a016d-174">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a016d-174">See Also</span></span>

[<span data-ttu-id="a016d-175">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="a016d-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="a016d-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a016d-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a016d-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a016d-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a016d-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a016d-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a016d-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="a016d-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="a016d-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="a016d-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="a016d-181">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="a016d-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="a016d-182">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="a016d-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a016d-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="a016d-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="a016d-184">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="a016d-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
