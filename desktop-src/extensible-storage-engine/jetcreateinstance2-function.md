---
description: 'Weitere Informationen finden Sie hier: JetCreateInstance2-Funktion'
title: JetCreateInstance2-Funktion
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359198"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="7cbd1-103">JetCreateInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cbd1-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="7cbd1-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7cbd1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="7cbd1-105">JetCreateInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="7cbd1-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="7cbd1-106">Die **JetCreateInstance2** -Funktion wird verwendet, um eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess zuzuordnen, wobei ein angegebener Anzeige Name angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="7cbd1-107">**Windows XP:**  **JetCreateInstance2** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7cbd1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cbd1-108">Parameters</span></span>

<span data-ttu-id="7cbd1-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="7cbd1-109">*pinstance*</span></span>

<span data-ttu-id="7cbd1-110">Der Ausgabepuffer, der die neu erstellte-Instanz empfängt.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="7cbd1-111">*szinstancename*</span><span class="sxs-lookup"><span data-stu-id="7cbd1-111">*szInstanceName*</span></span>

<span data-ttu-id="7cbd1-112">Gibt einen eindeutigen Zeichen folgen Bezeichner für die Instanz an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="7cbd1-113">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="7cbd1-114">**Hinweis** Ein NULL-Wert wird als gültiger Zeichen folgen Bezeichner für eine-Instanz behandelt.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="7cbd1-115">Es darf nur eine Instanz eine NULL-Zeichen folgen Kennung enthalten.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="7cbd1-116">*szDisplayName*</span><span class="sxs-lookup"><span data-stu-id="7cbd1-116">*szDisplayName*</span></span>

<span data-ttu-id="7cbd1-117">Ein Anzeige Name für die zu erstellende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-117">A display name for the instance to be created.</span></span> <span data-ttu-id="7cbd1-118">Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass sein Wert NULL ist.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="7cbd1-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7cbd1-119">*grbit*</span></span>

<span data-ttu-id="7cbd1-120">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-120">Reserved for future use.</span></span> <span data-ttu-id="7cbd1-121">Wenn dieser Parameter nicht vorhanden ist, wird davon ausgegangen, dass der Wert 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="7cbd1-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7cbd1-122">Return Value</span></span>

<span data-ttu-id="7cbd1-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7cbd1-124">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7cbd1-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cbd1-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7cbd1-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="7cbd1-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cbd1-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7cbd1-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7cbd1-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbd1-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="7cbd1-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="7cbd1-130">Der angegebene Instanzname wird bereits für diesen Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7cbd1-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7cbd1-132">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="7cbd1-133">Dies kann bei <a href="gg269354(v=exchg.10).md">jetkreateinstance</a> vorkommen, wenn <em>pinstance</em> NULL ist.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbd1-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="7cbd1-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="7cbd1-135">Der Vorgang ist fehlgeschlagen, weil er nicht verwendet werden kann, wenn die Datenbank-Engine im Einzel Instanz-Modus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="7cbd1-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="7cbd1-137">Es konnte keine neue Instanz erstellt werden, da die maximale Anzahl von Instanzen erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="7cbd1-138">Die maximale Anzahl unterstützter Instanzen wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mithilfe von <em>JET_paramMaxInstances</em>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7cbd1-139">Bei Erfolg wird eine neue Instanz zugewiesen, und der Bezeichner für die Instanz wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="7cbd1-140">An diesem Punkt verfügen alle Systemparameter für die-Instanz über die Werte der globalen Standardsystem Parameter.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="7cbd1-141">Sobald eine Instanz zugewiesen wird, muss Sie beendet und/oder später freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="7cbd1-142">Bei einem Fehler wird ein Fehler zurückgegeben, der die Ursache des Fehlers darstellt, und es wird keine Instanz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7cbd1-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cbd1-143">Remarks</span></span>

<span data-ttu-id="7cbd1-144">Eine Instanz muss mit einem [calltinit](./jetinit-function.md) -Namen initialisiert werden, bevor Sie von einem anderen als [jetsetsystemparameter](./jetsetsystemparameter-function.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="7cbd1-145">Eine Instanz wird durch einen-Rückruf der [jetterm](./jetterm-function.md) -Funktion zerstört, auch wenn diese Instanz nicht mit [jetinit](./jetinit-function.md)initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="7cbd1-146">Die maximale Anzahl von Instanzen, die zu einem beliebigen Zeitpunkt erstellt werden können, wird durch *JET_paramMaxInstances* gesteuert, der durch einen Aufruf von [jetsetsystemparameter](./jetsetsystemparameter-function.md)konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="7cbd1-147">Eine Instanz ist die Wiederherstellbarkeits Einheit für die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="7cbd1-148">Er steuert den Lebenszyklus aller Dateien, mit denen die Integrität der Daten in einem Satz von Datenbankdateien geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="7cbd1-149">Diese Dateien enthalten die Prüf Punkt Datei und die Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="7cbd1-150">Wenn die Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine als Nebeneffekt dieses Aufrufes automatisch in den Modus für mehrere Instanzen geändert.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="7cbd1-151">Wenn die Anwendung nur eine Instanz im Prozess zulassen möchte, sollte [jetinit](./jetinit-function.md) verwendet werden, um die Datenbank-Engine im Windows 2000-Kompatibilitätsmodus zu starten.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="7cbd1-152">Falls vorhanden, wird der *szDisplayName* -Parameter verwendet, um die Instanz an Stellen wie dem Ereignisprotokoll oder an andere Aufrufer wie Sicherungs Anwendungen zu identifizieren (durch Funktionen wie [jetgetinstanceinfo](./jetgetinstanceinfo-function.md) oder [jetossnapshotfreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7cbd1-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="7cbd1-153">Wenn der Anzeige Name nicht angegeben wird, wird stattdessen der eindeutige *szinstancename* -Parameter verwendet, sofern vorhanden. andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="7cbd1-154">Wenn für die Engine nicht der laufende Modus festgelegt wurde, wird Sie nach diesem-Befehl auf den Modus für mehrere Instanzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="7cbd1-155">Die typische Startsequenz für einen Prozess, bei dem möglicherweise mehrere Jet-Instanzen ausgeführt werden, wäre Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7cbd1-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="7cbd1-156">Ein **JetCreateInstance2** -Befehl, der die-Instanz zuweist und deren Namen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="7cbd1-157">Mehrere Aufrufe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) für diese Instanz, um unterschiedliche Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="7cbd1-158">Beachten Sie, dass einige Systemparameter für jede Instanz eindeutig sein müssen (wie z. b. *JET_paramSystemPath* oder *JET_paramLogFilePath*), sodass diese wahrscheinlich festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="7cbd1-159">Starten Sie die Instanz mit [jetinit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="7cbd1-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="7cbd1-160">Verwenden Sie [jetterm](./jetterm-function.md) oder [JetTerm2](./jetterm2-function.md), um eine Instanz zu beenden und/oder freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="7cbd1-161">Wenn dies die erste Instanz ist, die gestartet werden soll, gibt es eine Reihe zusätzlicher Schritte, die während dieses Aufrufes ausgeführt werden, um eine grundlegende Systeminitialisierung und Konfiguration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="7cbd1-162">Eine Reihe dieser Schritte führt möglicherweise zu bestimmten Fehlern, die mit JET_errOutOfMemory beginnen, aber auch andere (Weitere Informationen finden Sie unter Rückgabewerte).</span><span class="sxs-lookup"><span data-stu-id="7cbd1-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7cbd1-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cbd1-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-165">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbd1-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-167">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-169">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbd1-170"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-171">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cbd1-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-173">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7cbd1-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbd1-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7cbd1-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7cbd1-175">Implementiert als <strong>JetCreateInstance2W</strong> (Unicode) und <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7cbd1-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7cbd1-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7cbd1-176">See Also</span></span>

[<span data-ttu-id="7cbd1-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7cbd1-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7cbd1-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7cbd1-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7cbd1-179">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="7cbd1-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="7cbd1-180">Jetenablemultiinstance</span><span class="sxs-lookup"><span data-stu-id="7cbd1-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="7cbd1-181">Jetgetinstanceingefo</span><span class="sxs-lookup"><span data-stu-id="7cbd1-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="7cbd1-182">JetInit</span><span class="sxs-lookup"><span data-stu-id="7cbd1-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="7cbd1-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="7cbd1-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="7cbd1-184">Jeto ssnapshotfreeze</span><span class="sxs-lookup"><span data-stu-id="7cbd1-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="7cbd1-185">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="7cbd1-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7cbd1-186">Jetterm</span><span class="sxs-lookup"><span data-stu-id="7cbd1-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="7cbd1-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="7cbd1-187">JetTerm2</span></span>](./jetterm2-function.md)
