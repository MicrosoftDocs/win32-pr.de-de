---
description: 'Weitere Informationen zu: jetenablemultiinstance-Funktion'
title: Jetenablemultiinstance-Funktion
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373377"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="478c0-103">Jetenablemultiinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="478c0-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="478c0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="478c0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="478c0-105">Jetenablemultiinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="478c0-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="478c0-106">Die **jetenablemultiinstance** -Funktion konfiguriert die Datenbank-Engine für die Verwendung mit mehreren Instanzen im gleichen Prozess.</span><span class="sxs-lookup"><span data-stu-id="478c0-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="478c0-107">Ein optionales Array globaler Systemparameter ist für den ersten Aufrufer verfügbar, der die Änderung des Modus für mehrere Instanzen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="478c0-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="478c0-108">**Windows XP: jetenablemultiinstance** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="478c0-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="478c0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="478c0-109">Parameters</span></span>

<span data-ttu-id="478c0-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="478c0-110">*psetsysparam*</span></span>

<span data-ttu-id="478c0-111">Ein Array von globalen Systemparametern, das nur dann festgelegt werden soll, wenn die Engine als Ergebnis dieses Aufrufes in den multiinstanzmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="478c0-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="478c0-112">Wenn *csetsysparam* gleich 0 (null) ist, wird *psetsysparam* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="478c0-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="478c0-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="478c0-113">*csetsysparam*</span></span>

<span data-ttu-id="478c0-114">Die Anzahl der Elemente für das Array von globalen Parametern, die nur dann festgelegt werden sollen, wenn die Engine als Ergebnis dieses Aufrufes den Modus für mehrere Instanzen eingibt.</span><span class="sxs-lookup"><span data-stu-id="478c0-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="478c0-115">Wenn *csetsysparam* gleich 0 (null) ist, wird *psetsysparam* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="478c0-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="478c0-116">*pcseterfolg*</span><span class="sxs-lookup"><span data-stu-id="478c0-116">*pcsetsucceed*</span></span>

<span data-ttu-id="478c0-117">Ein Zeiger auf die Anzahl der globalen Systemparameter, die als Ergebnis dieses Aufrufes erfolgreich konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="478c0-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="478c0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="478c0-118">Return Value</span></span>

<span data-ttu-id="478c0-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="478c0-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="478c0-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="478c0-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="478c0-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="478c0-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="478c0-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="478c0-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="478c0-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="478c0-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="478c0-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="478c0-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478c0-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="478c0-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="478c0-126">Die angegebenen tupelindexparameter waren nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="478c0-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="478c0-127">Dieser Fehler kann von <strong>jetenablemultiinstance</strong> nur zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> auf einen ungültigen Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="478c0-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="478c0-128"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="478c0-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478c0-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="478c0-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="478c0-130">Der angegebene Dateisystempfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="478c0-130">The specified file system path was invalid.</span></span> <span data-ttu-id="478c0-131">Dieser Fehler kann von <strong>jetenablemultiinstance</strong> nur beim Festlegen von Systemparametern zurückgegeben werden, die Dateisystem Pfade darstellen.</span><span class="sxs-lookup"><span data-stu-id="478c0-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="478c0-132">Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> diesen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="478c0-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478c0-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="478c0-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="478c0-134">Der Vorgang ist fehlgeschlagen, da er unzulässig ist, wenn die Datenbank-Engine im einzelinstanzmodus (Windows 2000-Kompatibilitätsmodus) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="478c0-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478c0-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="478c0-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="478c0-136">Fehler bei <strong>jetenablemultiinstance</strong> , weil sich die Engine bereits im Modus für mehrere Instanzen befindet.</span><span class="sxs-lookup"><span data-stu-id="478c0-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="478c0-137"><strong>Hinweis  </strong> Dies geschieht auch, wenn keine Systemparameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="478c0-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="478c0-138">Wenn diese Funktion erfolgreich ausgeführt wird, wird die Datenbank-Engine so konfiguriert, dass Sie im Modus mit mehreren Instanzen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="478c0-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="478c0-139">Die Engine wurde auch erfolgreich mit der optionalen Liste der globalen Systemparameter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="478c0-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="478c0-140">Wenn diese Funktion fehlschlägt, verbleibt die Datenbank-Engine im aktuellen Modus.</span><span class="sxs-lookup"><span data-stu-id="478c0-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="478c0-141">Wenn *pcseterfolg* ungleich 0 (null) ist, bleibt diese Anzahl von Systemparametern festgelegt.</span><span class="sxs-lookup"><span data-stu-id="478c0-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="478c0-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="478c0-142">Remarks</span></span>

<span data-ttu-id="478c0-143">Diese Funktion sollte nur verwendet werden, wenn die Anwendung einen bestimmten Satz von Systemparametern atomarisch konfigurieren muss, wenn die Datenbank-Engine für die Verwendung in einem Szenario mit mehreren Benutzern in demselben Prozess eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="478c0-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="478c0-144">Wenn eine andere Synchronisierungsmethode verfügbar ist, ist es vorzuziehen, [jetkreateinstance](./jetcreateinstance-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md) separat aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="478c0-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="478c0-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="478c0-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="478c0-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-147">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="478c0-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478c0-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-149">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="478c0-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478c0-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-151">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="478c0-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478c0-152"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-153">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="478c0-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="478c0-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-155">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="478c0-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478c0-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="478c0-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="478c0-157">Implementiert als <strong>jetenablemultiinstancew</strong> (Unicode) und <strong>jetenablemultiinstancea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="478c0-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="478c0-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="478c0-158">See Also</span></span>

[<span data-ttu-id="478c0-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="478c0-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="478c0-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="478c0-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="478c0-161">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="478c0-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="478c0-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="478c0-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="478c0-163">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="478c0-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
