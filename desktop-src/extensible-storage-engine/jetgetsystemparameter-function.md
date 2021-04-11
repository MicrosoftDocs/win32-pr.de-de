---
description: 'Weitere Informationen: jetgetsystemparameter-Funktion'
title: Jetgetsystemparameter-Funktion
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217852"
---
# <a name="jetgetsystemparameter-function"></a><span data-ttu-id="7ee7e-103">Jetgetsystemparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ee7e-103">JetGetSystemParameter Function</span></span>


<span data-ttu-id="7ee7e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ee7e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsystemparameter-function"></a><span data-ttu-id="7ee7e-105">Jetgetsystemparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ee7e-105">JetGetSystemParameter Function</span></span>

<span data-ttu-id="7ee7e-106">Die **jetgetsystemparameter** -Funktion liest die zahlreichen Konfigurationseinstellungen der Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-106">The **JetGetSystemParameter** function reads the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="7ee7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ee7e-107">Parameters</span></span>

<span data-ttu-id="7ee7e-108">*lichen*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-108">*instance*</span></span>

<span data-ttu-id="7ee7e-109">Die-Instanz, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-109">The instance to use for this call.</span></span>

<span data-ttu-id="7ee7e-110">Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **null** sein.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-110">For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="7ee7e-111">Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-111">For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="7ee7e-112">Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="7ee7e-113">In beiden Fällen werden alle Systemparameter Einstellungen aus dieser eine Instanz gelesen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="7ee7e-114">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, kann dieser Parameter **null** sein, oder es handelt sich um einen Zeiger auf eine Instanz, die mit [jetinit](./jetinit-function.md) oder [jetkreateinstance](./jetcreateinstance-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-114">If the engine is operating in multi-instance mode, this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateInstance](./jetcreateinstance-function.md).</span></span> <span data-ttu-id="7ee7e-115">Wenn dieser Parameter **null** ist, wird die Parametereinstellung des globalen Systems (oder der Standardwert) gelesen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="7ee7e-116">Wenn dieser Parameter eine Instanz ist, wird die Systemparameter Einstellung für diese Instanz gelesen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="7ee7e-117">*-sid*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-117">*sesid*</span></span>

<span data-ttu-id="7ee7e-118">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-118">The session to use for this call.</span></span>

<span data-ttu-id="7ee7e-119">Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-119">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="7ee7e-120">*paramid*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-120">*paramid*</span></span>

<span data-ttu-id="7ee7e-121">Die ID des System Parameters, der gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-121">The ID of the system parameter that will be read.</span></span>

<span data-ttu-id="7ee7e-122">Eine komplette Liste der Systemparameter und deren Eigenschaften finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee7e-122">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="7ee7e-123">*plparam*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-123">*plParam*</span></span>

<span data-ttu-id="7ee7e-124">Der Ausgabepuffer, der den Wert des ausgewählten System Parameters empfängt, wenn dieser Systemparameter einen ganzzahligen Typ hat.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-124">The output buffer that receives the value of the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="7ee7e-125">*szparam*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-125">*szParam*</span></span>

<span data-ttu-id="7ee7e-126">Der Ausgabepuffer, der den Wert des ausgewählten System Parameters empfängt, wenn dieser Systemparameter vom Typ String ist.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-126">The output buffer that receives the value of the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="7ee7e-127">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="7ee7e-127">*cbMax*</span></span>

<span data-ttu-id="7ee7e-128">Die maximale Größe des Zeichen folgen-Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-128">The maximum size in bytes of the string output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="7ee7e-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ee7e-129">Return Value</span></span>

<span data-ttu-id="7ee7e-130">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7ee7e-131">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7ee7e-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ee7e-132">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7ee7e-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="7ee7e-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ee7e-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7ee7e-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-135">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7ee7e-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-137">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-138">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="7ee7e-138">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-139">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-139">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7ee7e-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-141">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="7ee7e-142">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7ee7e-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-144">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="7ee7e-145">Dies kann für <strong>jetgetsystemparameter</strong> auftreten, wenn:</span><span class="sxs-lookup"><span data-stu-id="7ee7e-145">This can happen for <strong>JetGetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="7ee7e-146">Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-146">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-147">Der angegebene Systemparameter erfordert, dass der ganzzahlige Ausgabepuffer bereitgestellt wird und dass der Ausgabepuffer Zeiger <strong>null</strong>war.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-147">The specified system parameter requires the integer output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-148">Der angegebene Systemparameter erfordert, dass ein Zeichen folgen-Ausgabepuffer angegeben wird und dass der Ausgabepuffer Zeiger <strong>null</strong>war.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-148">The specified system parameter requires a string output buffer to be provided and that output buffer pointer was <strong>NULL</strong>.</span></span></p>
<p><span data-ttu-id="7ee7e-149"><strong>Windows Vista:  </strong> Dies kann nur in Windows Vista und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-149"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-150">Der angegebene Systemparameter erfordert, dass ein Zeichen folgen-Ausgabepuffer angegeben wird, und die Größe dieses Ausgabepuffers ist zu klein, um eine NULL-terminierte Zeichenfolge zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-150">The specified system parameter requires a string output buffer to be provided and the size of that output buffer is too small to accept a null terminated string.</span></span></p>
<p><span data-ttu-id="7ee7e-151"><strong>Windows Vista:  </strong> Dies kann nur in Windows Vista und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-151"><strong>Windows Vista:  </strong>This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-152">Der angegebene Systemparameter kann nicht gelesen werden, da er schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-152">The specified system parameter cannot be read because it is write-only.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-153">Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-153">The specified system parameter is global only and an attempt was made to read an instance specific value for that system parameter.</span></span> <span data-ttu-id="7ee7e-154">Dies kann nur unter Windows XP und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-154">This can only happen on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="7ee7e-155">Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-155">The specified system parameter is per-instance only and an attempt was made to read the global value for that system parameter.</span></span> <span data-ttu-id="7ee7e-156">Dies kann nur unter Windows XP und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-156">This can only happen on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-157">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7ee7e-157">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-158">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-158">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-159">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7ee7e-159">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-160">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-160">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7ee7e-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-162">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-163">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="7ee7e-163">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-164">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-164">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="7ee7e-165">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="7ee7e-166">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-167">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="7ee7e-167">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-168">Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-168">The instance handle is invalid or refers to an instance that has been shutdown.</span></span> <span data-ttu-id="7ee7e-169">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-169">This error is not returned under all circumstances.</span></span> <span data-ttu-id="7ee7e-170">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-170">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="7ee7e-171"><strong>Windows Vista:  </strong> Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-171"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-172">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="7ee7e-172">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-173">Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um die gesamte Systemparameter Einstellung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-173">The operation completed successfully, but the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="7ee7e-174">Der Ausgabepuffer wurde mit dem Umfang der Systemparameter Einstellung aufgefüllt, wie er passt.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-174">The output buffer has been filled with as much of the system parameter setting as would fit.</span></span> <span data-ttu-id="7ee7e-175">Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer Null beendet.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-175">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="7ee7e-176"><strong>Hinweis  </strong> Dieser Fehler wird nicht von allen Releases zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-176"><strong>Note  </strong>This error is not returned by all releases.</span></span> <span data-ttu-id="7ee7e-177">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7ee7e-177">Please see the Remarks section for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="7ee7e-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="7ee7e-179">Der Vorgang ist fehlgeschlagen, weil der Ausgabepuffer zu klein war, um die gesamte Systemparameter Einstellung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-179">The operation failed because the output buffer was too small to receive the entire system parameter setting.</span></span></p>
<p><span data-ttu-id="7ee7e-180"><strong>Hinweis  </strong> Dieser Fehler wird in einigen Fällen nicht zurückgegeben, um die Anwendungs Kompatibilität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-180"><strong>Note  </strong>This error is not returned in some cases to preserve application compatibility.</span></span> <span data-ttu-id="7ee7e-181">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7ee7e-181">Please see the Remarks section for more information.</span></span></p>
<p><span data-ttu-id="7ee7e-182"><strong>Windows Vista:  </strong> Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-182"><strong>Windows Vista:  </strong>This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ee7e-183">Bei Erfolg wird der für den angeforderten Systemparameter geeignete Ausgabepuffer auf den Wert dieses System Parameters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-183">On success, the output buffer appropriate for the requested system parameter will be set to the value of that system parameter.</span></span>

<span data-ttu-id="7ee7e-184">Bei einem Fehler wird der Status der Ausgabepuffer nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-184">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7ee7e-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ee7e-185">Remarks</span></span>

<span data-ttu-id="7ee7e-186">In dieser API gibt es ein wichtiges Problem, das in allen Releases vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-186">There is an important problem in this API that is present in all releases.</span></span> <span data-ttu-id="7ee7e-187">Wenn ein Systemparameter mit einem Zeichen folgen Wert angefordert wird und der Ausgabepuffer zu klein ist, um die gesamte Systemparameter Einstellung zu erhalten, werden keine JET_wrnBufferTruncated zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-187">If a system parameter with a string value is requested and the output buffer is too small to receive the entire system parameter setting, JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="7ee7e-188">Stattdessen wird JET_errSuccess zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-188">JET_errSuccess is returned instead.</span></span> <span data-ttu-id="7ee7e-189">Wenn die Länge der zurückgegebenen Zeichenfolge der Größe des Ausgabepuffers abzüglich des **null** -Terminator entspricht, sollte der Aufrufer so reagieren, als ob JET_wrnBufferTruncated zurückgegeben würden.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-189">If the length of the returned string is equal to the size of the output buffer less the **NULL** terminator, the caller should react as if JET_wrnBufferTruncated were returned.</span></span> <span data-ttu-id="7ee7e-190">Wenn ein Ausgabepuffer der Größe 0 (null) angegeben wird, sollte der Aufrufer so reagieren, als ob JET_errInvalidParameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-190">If a zero-sized string output buffer is specified, the caller should react as if JET_errInvalidParameter were returned.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7ee7e-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ee7e-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-193">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-195">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-198"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-199">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ee7e-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-201">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7ee7e-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ee7e-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7ee7e-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7ee7e-203">Implementiert als <strong>jetgetsystemparameterw</strong> (Unicode) und <strong>jetgetsystemparametera</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7ee7e-203">Implemented as <strong>JetGetSystemParameterW</strong> (Unicode) and <strong>JetGetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7ee7e-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7ee7e-204">See Also</span></span>

[<span data-ttu-id="7ee7e-205">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="7ee7e-205">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="7ee7e-206">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7ee7e-206">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7ee7e-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7ee7e-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7ee7e-208">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7ee7e-208">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7ee7e-209">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="7ee7e-209">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="7ee7e-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="7ee7e-210">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="7ee7e-211">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="7ee7e-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7ee7e-212">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="7ee7e-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="7ee7e-213">System Parameter</span><span class="sxs-lookup"><span data-stu-id="7ee7e-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
