---
description: 'Weitere Informationen zu: jetkreateinzustance-Funktion'
title: JetCreateInstance-Funktion
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366484"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="06016-103">JetCreateInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="06016-103">JetCreateInstance Function</span></span>


<span data-ttu-id="06016-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06016-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="06016-105">JetCreateInstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="06016-105">JetCreateInstance Function</span></span>

<span data-ttu-id="06016-106">Die **jetkreateinstance** -Funktion weist eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess zu.</span><span class="sxs-lookup"><span data-stu-id="06016-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="06016-107">**Windows XP: jetkreateinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="06016-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="06016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06016-108">Parameters</span></span>

<span data-ttu-id="06016-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="06016-109">*pinstance*</span></span>

<span data-ttu-id="06016-110">Der Ausgabepuffer, der die neu erstellte-Instanz empfängt.</span><span class="sxs-lookup"><span data-stu-id="06016-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="06016-111">*szinstancename*</span><span class="sxs-lookup"><span data-stu-id="06016-111">*szInstanceName*</span></span>

<span data-ttu-id="06016-112">Ein eindeutiger Zeichen folgen Bezeichner für die zu erstellende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="06016-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="06016-113">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="06016-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="06016-114">**Hinweis** Ein NULL-Wert wird als gültiger Zeichen folgen Bezeichner für eine-Instanz behandelt.</span><span class="sxs-lookup"><span data-stu-id="06016-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="06016-115">Es darf nur eine Instanz eine NULL-Zeichen folgen Kennung enthalten.</span><span class="sxs-lookup"><span data-stu-id="06016-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="06016-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06016-116">Return Value</span></span>

<span data-ttu-id="06016-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="06016-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="06016-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="06016-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06016-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="06016-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="06016-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06016-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06016-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="06016-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="06016-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="06016-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06016-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="06016-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="06016-124">Der angegebene Instanzname wird bereits für diesen Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="06016-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06016-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="06016-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="06016-126">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="06016-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="06016-127">Dies kann bei <strong>jetkreateinstance</strong> vorkommen, wenn <em>pinstance</em> <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="06016-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06016-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="06016-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="06016-129">Der Vorgang ist fehlgeschlagen, weil er nicht verwendet werden kann, wenn die Datenbank-Engine im Einzel Instanz-Modus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06016-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06016-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="06016-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="06016-131">Es konnte keine neue Instanz erstellt werden, da die maximale Anzahl von Instanzen erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="06016-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="06016-132">Die maximale Anzahl unterstützter Instanzen wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mithilfe von <em>JET_paramMaxInstances</em>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="06016-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06016-133">Bei Erfolg wird eine neue Instanz zugewiesen, und der Bezeichner für die Instanz wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06016-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="06016-134">An diesem Punkt verfügen alle Systemparameter für die-Instanz über die Werte der globalen Standardsystem Parameter.</span><span class="sxs-lookup"><span data-stu-id="06016-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="06016-135">Sobald eine Instanz zugewiesen wird, muss Sie beendet und/oder später freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06016-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="06016-136">Bei einem Fehler wird ein Fehler zurückgegeben, der die Ursache des Fehlers darstellt, und es wird keine Instanz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="06016-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="06016-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06016-137">Remarks</span></span>

<span data-ttu-id="06016-138">Eine Instanz muss mit einem [calltinit](./jetinit-function.md) -Namen initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="06016-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="06016-139">Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit [jetinit](./jetinit-function.md)initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="06016-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="06016-140">Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch [JET_paramMaxInstances](./resource-parameters.md)gesteuert, der durch einen Aufruf von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="06016-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="06016-141">Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="06016-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="06016-142">Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="06016-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="06016-143">Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="06016-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="06016-144">Wenn die Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine als Nebeneffekt dieses Aufrufes automatisch in den Modus für mehrere Instanzen geändert.</span><span class="sxs-lookup"><span data-stu-id="06016-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="06016-145">Wenn die Anwendung nur eine Instanz im Prozess zulassen möchte, sollte [jetinit](./jetinit-function.md) verwendet werden, um die Datenbank-Engine im Windows 2000-Kompatibilitätsmodus zu starten.</span><span class="sxs-lookup"><span data-stu-id="06016-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="06016-146">Falls vorhanden, wird der *szDisplayName* verwendet, um die Instanz an Orten wie dem Ereignisprotokoll oder an anderen Aufrufern wie Sicherungs Anwendungen (über Funktionen wie [jetgetinstanceinfo](./jetgetinstanceinfo-function.md) oder [jetossnapshotfreeze](./jetossnapshotfreeze-function.md)) zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="06016-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="06016-147">Wenn der Anzeige Name nicht angegeben wird, wird stattdessen der eindeutige *szinstancename* verwendet, sofern vorhanden. andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06016-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="06016-148">Wenn für die Engine nicht der laufende Modus festgelegt wurde, wird Sie nach diesem-Befehl auf den Modus für mehrere Instanzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06016-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="06016-149">Die typische Startsequenz für einen Prozess, bei dem möglicherweise mehrere Jet-Instanzen ausgeführt werden, wäre Folgendes:</span><span class="sxs-lookup"><span data-stu-id="06016-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="06016-150">Ein [JetCreateInstance2](./jetcreateinstance2-function.md) -Befehl, der die-Instanz zuweist und deren Namen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="06016-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="06016-151">Mehrere Aufrufe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) für diese Instanz, um unterschiedliche Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="06016-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="06016-152">Beachten Sie, dass einige Systemparameter pro Instanz eindeutig sein müssen (wie z. b. [JET_paramSystemPath](./transaction-log-parameters.md) oder [JET_paramLogFilePath](./transaction-log-parameters.md)), sodass wahrscheinlich eine dieser Parameter festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="06016-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="06016-153">Starten Sie die Instanz mit [jetinit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="06016-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="06016-154">Um eine Instanz zu beenden und/oder freizugeben, muss [jetterm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06016-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="06016-155">Wenn dies die erste Instanz ist, die gestartet werden soll, gibt es eine Reihe zusätzlicher Schritte, die während dieses Aufrufes ausgeführt werden, um eine grundlegende Systeminitialisierung und Konfiguration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="06016-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="06016-156">Einige dieser Schritte können zu bestimmten Fehlern führen, die mit JET_errOutOfMemory beginnen, aber auch andere (siehe Fehler oben).</span><span class="sxs-lookup"><span data-stu-id="06016-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="06016-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06016-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06016-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="06016-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-159">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06016-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06016-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="06016-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-161">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="06016-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06016-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="06016-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-163">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="06016-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06016-164"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="06016-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-165">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="06016-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06016-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="06016-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-167">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="06016-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06016-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="06016-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="06016-169">Implementiert als <strong>jetkreateingestancew</strong> (Unicode) und <strong>jetkreateingestancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="06016-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="06016-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06016-170">See Also</span></span>

[<span data-ttu-id="06016-171">Extensible Storage Engine-Dateien</span><span class="sxs-lookup"><span data-stu-id="06016-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="06016-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="06016-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="06016-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="06016-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="06016-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="06016-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="06016-175">Jetenablemultiinstance</span><span class="sxs-lookup"><span data-stu-id="06016-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="06016-176">Jetgetinstanceingefo</span><span class="sxs-lookup"><span data-stu-id="06016-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="06016-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="06016-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="06016-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="06016-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="06016-179">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="06016-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="06016-180">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="06016-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="06016-181">Jetterm</span><span class="sxs-lookup"><span data-stu-id="06016-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="06016-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="06016-182">JetTerm2</span></span>](./jetterm2-function.md)
