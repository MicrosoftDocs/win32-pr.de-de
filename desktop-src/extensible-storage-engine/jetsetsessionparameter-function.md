---
description: Weitere Informationen finden Sie in der jetabessionparameter-Funktion
title: Jetabessionparameter-Funktion
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958793"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="49ddd-103">Jetabessionparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="49ddd-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="49ddd-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49ddd-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="49ddd-105">Die **Jet** -Sitzungs Parameter-Funktion konfiguriert die Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="49ddd-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="49ddd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49ddd-106">Parameters</span></span>

<span data-ttu-id="49ddd-107">*-sid*</span><span class="sxs-lookup"><span data-stu-id="49ddd-107">*sesid*</span></span>

<span data-ttu-id="49ddd-108">Gibt die Sitzung an, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49ddd-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="49ddd-109">Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="49ddd-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="49ddd-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="49ddd-110">*sesparamid*</span></span>

<span data-ttu-id="49ddd-111">Die ID des festzulegenden Sitzungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="49ddd-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="49ddd-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="49ddd-112">*pvParam*</span></span>

<span data-ttu-id="49ddd-113">Die in diesem Sitzungs Parameter festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="49ddd-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="49ddd-114">*cbparam*</span><span class="sxs-lookup"><span data-stu-id="49ddd-114">*cbParam*</span></span>

<span data-ttu-id="49ddd-115">Die Größe der bereitgestellten Daten.</span><span class="sxs-lookup"><span data-stu-id="49ddd-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="49ddd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49ddd-116">Return value</span></span>

<span data-ttu-id="49ddd-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="49ddd-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="49ddd-118">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="49ddd-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49ddd-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="49ddd-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="49ddd-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49ddd-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="49ddd-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="49ddd-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="49ddd-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="49ddd-124">Die Instanz wurde mithilfe eines Aufrufens der <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion initialisiert, und dieser Vorgang kann nicht als Ergebnis ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="49ddd-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="49ddd-125">Dies kann vorkommen, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Parameter Werts nicht mehr den Status der Datenbank-Engine beeinflussen kann.</span><span class="sxs-lookup"><span data-stu-id="49ddd-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="49ddd-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="49ddd-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="49ddd-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="49ddd-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="49ddd-129">Die angegebenen tupelindexparameter waren unzulässig.</span><span class="sxs-lookup"><span data-stu-id="49ddd-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="49ddd-130">Dieser Fehler wird nur zurückgegeben, wenn der <em>JET_paramIndexTuplesLengthMin</em>-, <em>JET_paramIndexTuplesLengthMax</em>-oder <em>JET_paramIndexTuplesToIndexMax</em> -Parameter auf einen unzulässigen Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="49ddd-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="49ddd-131">Weitere Informationen zu diesen Parametern finden Sie unter <a href="gg294119(v=exchg.10).md">index Parameter</a>.</span><span class="sxs-lookup"><span data-stu-id="49ddd-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="49ddd-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="49ddd-133">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="49ddd-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="49ddd-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="49ddd-135">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="49ddd-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="49ddd-137">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="49ddd-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="49ddd-138">Dies kann vorkommen, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="49ddd-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="49ddd-139">Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49ddd-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-140">Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einer Zeichenfolge festzulegen, deren Länge außerhalb des gültigen Bereichs für den Parameter lag.</span><span class="sxs-lookup"><span data-stu-id="49ddd-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-141">Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einem Dateipfad festzulegen, bei dem die Länge der absoluten Pfad Darstellung außerhalb des gültigen Bereichs für diesen Parameter liegt.</span><span class="sxs-lookup"><span data-stu-id="49ddd-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-142">Es wurde versucht, einen ganzzahligen Wert mit einem ganzzahligen Wert festzulegen, der außerhalb des gültigen Bereichs für den Parameter liegt.</span><span class="sxs-lookup"><span data-stu-id="49ddd-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-143">Es wurde versucht, JET_paramUnicodeIndexDefault mit einem NULL- <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Zeiger, einer ungültigen LCID oder einem nicht unterstützten Satz von <strong>LCMapString</strong> -Flags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-144">Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="49ddd-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-145">Es wurde versucht, einen Systemparameter festzulegen, nachdem die <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion aufgerufen wurde, die Datenbank-Engine sich im Einzel Instanz-Modus befindet und keine Sitzung angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="49ddd-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-146">Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="49ddd-147">Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="49ddd-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="49ddd-149">Der angegebene Dateisystempfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="49ddd-149">The specified file system path was invalid.</span></span> <span data-ttu-id="49ddd-150">Dieser Fehler wird möglicherweise nur von <strong>jetdeptessionparameter</strong> zurückgegeben, wenn Systemparameter festgelegt werden, die Dateisystem Pfade darstellen.</span><span class="sxs-lookup"><span data-stu-id="49ddd-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="49ddd-151">Beispielsweise kann der <em>JET_paramSystemPath</em> -Parameter diesen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49ddd-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="49ddd-152">Weitere Informationen zu diesem Parameter finden Sie unter <a href="gg269235(v=exchg.10).md">Transaktionsprotokoll Parameter</a>.</span><span class="sxs-lookup"><span data-stu-id="49ddd-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="49ddd-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="49ddd-154">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49ddd-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="49ddd-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="49ddd-156">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49ddd-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="49ddd-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="49ddd-158">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="49ddd-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="49ddd-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="49ddd-160">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="49ddd-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="49ddd-161">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49ddd-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="49ddd-162">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="49ddd-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="49ddd-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="49ddd-164">Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="49ddd-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="49ddd-165">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49ddd-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="49ddd-166">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="49ddd-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49ddd-167">Bei Erfolg wird der Systemparameter auf den bereitgestellten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49ddd-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="49ddd-168">Bei einem Fehler bleibt der Wert des System Parameters unverändert.</span><span class="sxs-lookup"><span data-stu-id="49ddd-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="49ddd-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49ddd-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="49ddd-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49ddd-171">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49ddd-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-172"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="49ddd-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49ddd-173">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="49ddd-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-174"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="49ddd-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49ddd-175">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="49ddd-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49ddd-176"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="49ddd-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="49ddd-177">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="49ddd-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49ddd-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="49ddd-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="49ddd-179">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="49ddd-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="49ddd-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ddd-180">See also</span></span>

[<span data-ttu-id="49ddd-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="49ddd-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="49ddd-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49ddd-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49ddd-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="49ddd-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="49ddd-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="49ddd-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="49ddd-185">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="49ddd-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="49ddd-186">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="49ddd-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="49ddd-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="49ddd-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="49ddd-188">System Parameter</span><span class="sxs-lookup"><span data-stu-id="49ddd-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
