---
description: 'Weitere Informationen zu: jetsetsystemparameter-Funktion'
title: Jetsetsystemparameter-Funktion
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214754"
---
# <a name="jetsetsystemparameter-function"></a><span data-ttu-id="5837e-103">Jetsetsystemparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="5837e-103">JetSetSystemParameter Function</span></span>


<span data-ttu-id="5837e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5837e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsystemparameter-function"></a><span data-ttu-id="5837e-105">Jetsetsystemparameter-Funktion</span><span class="sxs-lookup"><span data-stu-id="5837e-105">JetSetSystemParameter Function</span></span>

<span data-ttu-id="5837e-106">Die **jetsetsystemparameter** -Funktion wird verwendet, um die zahlreichen Konfigurationseinstellungen der Datenbank-Engine festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5837e-106">The **JetSetSystemParameter** function is used to set the numerous configuration settings of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a><span data-ttu-id="5837e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5837e-107">Parameters</span></span>

<span data-ttu-id="5837e-108">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="5837e-108">*pinstance*</span></span>

<span data-ttu-id="5837e-109">Gibt die-Instanz an, die für diesen Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5837e-109">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="5837e-110">**Windows 2000:**  Für Windows 2000 wird dieser Parameter ignoriert und sollte immer **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5837e-110">**Windows 2000:**  For Windows 2000, this parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="5837e-111">**Windows XP:**  Für Windows XP und spätere Versionen ist dieser Parameter etwas überladen.</span><span class="sxs-lookup"><span data-stu-id="5837e-111">**Windows XP:**  For Windows XP and later releases, this parameter is somewhat overloaded.</span></span> <span data-ttu-id="5837e-112">Wenn die Engine im Legacy Modus betrieben wird (Windows 2000-Kompatibilitätsmodus), in dem nur eine Instanz unterstützt wird, kann dieser Parameter **null** sein oder die tatsächliche Instanz enthalten, die von [jetinit](./jetinit-function.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-112">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter may be **NULL** or may contain the actual instance returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="5837e-113">In beiden Fällen werden alle Systemparameter Einstellungen aus dieser eine Instanz gelesen.</span><span class="sxs-lookup"><span data-stu-id="5837e-113">In either case, all system parameter settings are read from that one instance.</span></span> <span data-ttu-id="5837e-114">Wenn die Engine im Modus für mehrere Instanzen ausgeführt wird, kann dieser Parameter **null** sein, oder es handelt sich um einen Zeiger auf eine Instanz, die mit [jetinit](./jetinit-function.md) oder [jetkreateindex](./jetcreateindex-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5837e-114">If the engine is operating in multi-instance mode, then this parameter may be **NULL** or a pointer to an instance created using [JetInit](./jetinit-function.md) or [JetCreateIndex](./jetcreateindex-function.md).</span></span> <span data-ttu-id="5837e-115">Wenn dieser Parameter **null** ist, wird die Parametereinstellung des globalen Systems (oder der Standardwert) gelesen.</span><span class="sxs-lookup"><span data-stu-id="5837e-115">When this parameter is **NULL** then the global system parameter setting (or default) is read.</span></span> <span data-ttu-id="5837e-116">Wenn dieser Parameter eine Instanz ist, wird die Systemparameter Einstellung für diese Instanz gelesen.</span><span class="sxs-lookup"><span data-stu-id="5837e-116">When this parameter is an instance then the system parameter setting for that instance is read.</span></span>

<span data-ttu-id="5837e-117">Obwohl es sich technisch gesehen um einen out-Parameter handelt, ändert diese API niemals den Inhalt des bereitgestellten Puffers.</span><span class="sxs-lookup"><span data-stu-id="5837e-117">Even though this is technically an out parameter, this API never modifies the contents of the provided buffer.</span></span>

<span data-ttu-id="5837e-118">*-sid*</span><span class="sxs-lookup"><span data-stu-id="5837e-118">*sesid*</span></span>

<span data-ttu-id="5837e-119">Gibt die Sitzung an, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5837e-119">Specifies the session to use for this call.</span></span>

<span data-ttu-id="5837e-120">Wenn angegeben, wird die angegebene-Instanz ignoriert, und die-Instanz, die der Sitzung zugeordnet ist, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="5837e-120">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="5837e-121">*paramid*</span><span class="sxs-lookup"><span data-stu-id="5837e-121">*paramid*</span></span>

<span data-ttu-id="5837e-122">Die ID des System Parameters, der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-122">The ID of the system parameter that will be set.</span></span> <span data-ttu-id="5837e-123">Eine komplette Liste der Systemparameter und deren Eigenschaften finden Sie unter [Systemparameter](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="5837e-123">See [System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="5837e-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5837e-124">*lParam*</span></span>

<span data-ttu-id="5837e-125">Gibt den Wert an, der für den ausgewählten Systemparameter festgelegt werden soll, wenn der Systemparameter einen ganzzahligen Typ hat.</span><span class="sxs-lookup"><span data-stu-id="5837e-125">Provides the value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="5837e-126">*szparam*</span><span class="sxs-lookup"><span data-stu-id="5837e-126">*szParam*</span></span>

<span data-ttu-id="5837e-127">Gibt den Wert für den ausgewählten Systemparameter an, wenn dieser Systemparameter vom Typ String ist.</span><span class="sxs-lookup"><span data-stu-id="5837e-127">Provides the value for the selected system parameter if that system parameter is of a string type.</span></span>

### <a name="return-value"></a><span data-ttu-id="5837e-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5837e-128">Return Value</span></span>

<span data-ttu-id="5837e-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="5837e-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5837e-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5837e-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5837e-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5837e-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="5837e-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5837e-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5837e-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5837e-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5837e-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5837e-134">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="5837e-135"><strong>Windows Vista:</strong>  Unter Windows Vista und höheren Versionen kann Erfolg zurückgegeben werden, ohne dass der Wert des System Parameters geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5837e-135"><strong>Windows Vista:</strong>  On Windows Vista and later releases, success can be returned without a change to the system parameter's value.</span></span> <span data-ttu-id="5837e-136">Weitere Informationen finden Sie im Abschnitt "JET_paramEnableAdvanced System" im Thema " <a href="gg269346(v=exchg.10).md">Meta para</a> meters".</span><span class="sxs-lookup"><span data-stu-id="5837e-136">See the JET_paramEnableAdvanced system parameter in the <a href="gg269346(v=exchg.10).md">Meta Parameters</a> topic for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-137">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="5837e-137">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="5837e-138">Die Instanz wurde mithilfe eines <a href="gg294068(v=exchg.10).md">jetinit-Aufrufes</a> initialisiert, und dieser Vorgang kann nicht als Ergebnis ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5837e-138">The instance has been initialized using a call to <a href="gg294068(v=exchg.10).md">JetInit</a> and this operation cannot be performed as a result.</span></span> <span data-ttu-id="5837e-139">Dies kann bei einem <strong>jetsetsystemparameter</strong> vorkommen, wenn versucht wird, einen Systemparameter zu konfigurieren, nachdem eine Änderung des Werts den Status der Datenbank-Engine nicht beeinträchtigt hat.</span><span class="sxs-lookup"><span data-stu-id="5837e-139">This can happen for <strong>JetSetSystemParameter</strong> when an attempt is made to configure a system parameter after a change in its value cannot affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5837e-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5837e-141">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5837e-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-142">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="5837e-142">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="5837e-143">Die angegebenen tupelindexparameter waren unzulässig.</span><span class="sxs-lookup"><span data-stu-id="5837e-143">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="5837e-144">Dieser Fehler kann von <strong>jetsetsystemparameter</strong> nur zurückgegeben werden, wenn <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>oder <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> auf einen ungültigen Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-144">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="5837e-145"><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-145"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-146">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="5837e-146">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="5837e-147">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-147">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5837e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5837e-149">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="5837e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5837e-150"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-150"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-151">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5837e-151">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5837e-152">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="5837e-152">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="5837e-153">Dies kann bei <strong>jetsetsystemparameter</strong> vorkommen, wenn:</span><span class="sxs-lookup"><span data-stu-id="5837e-153">This can happen for <strong>JetSetSystemParameter</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="5837e-154">Die angegebene Systemparameter-ID ist ungültig oder wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5837e-154">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="5837e-155">Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einer Zeichenfolge festzulegen, deren Länge außerhalb des gültigen Bereichs für den Parameter liegt.</span><span class="sxs-lookup"><span data-stu-id="5837e-155">An attempt was made to set a string-valued system parameter with a string whose length was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="5837e-156">Es wurde versucht, einen Systemparameter mit Zeichen folgen Wert mit einem Dateipfad festzulegen, bei dem die Länge der absoluten Pfad Darstellung außerhalb des gültigen Bereichs für diesen Parameter liegt.</span><span class="sxs-lookup"><span data-stu-id="5837e-156">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p>
<p><span data-ttu-id="5837e-157"><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-157"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="5837e-158">Es wurde versucht, einen ganzzahligen Wert mit einem ganzzahligen Wert festzulegen, der außerhalb des gültigen Bereichs für den Parameter liegt.</span><span class="sxs-lookup"><span data-stu-id="5837e-158">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="5837e-159">Es wurde versucht, JET_paramUnicodeIndexDefault mit einem NULL- <strong></strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Zeiger, einer ungültigen LCID oder einem nicht unterstützten Satz von LCMapString-Flags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5837e-159">An attempt was made to set JET_paramUnicodeIndexDefault with a <strong>NULL</strong> <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of LCMapString flags.</span></span></p>
<p><span data-ttu-id="5837e-160"><strong>Windows Vista:</strong>  Dies kann nur in Windows Vista und höheren Versionen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-160"><strong>Windows Vista:</strong>  This can only happen on Windows Vista and later releases.</span></span></p></li>
<li><p><span data-ttu-id="5837e-161">Der angegebene Systemparameter kann nicht festgelegt werden, da er schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="5837e-161">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="5837e-162">Es wurde versucht, einen Systemparameter festzulegen, nachdem <a href="gg294068(v=exchg.10).md">jetinit</a> aufgerufen wurde, die Datenbank-Engine befindet sich im Einzel Instanz-Modus, und es wurde keine Sitzung angegeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-162">An attempt was made to set a system parameter after <a href="gg294068(v=exchg.10).md">JetInit</a> was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p>
<p><span data-ttu-id="5837e-163"><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-163"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="5837e-164">Der angegebene Systemparameter ist nur global und es wurde versucht, einen instanzspezifischen Wert für diesen Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5837e-164">The specified system parameter is global only and an attempt was made to set an instance specific value for that system parameter.</span></span></p>
<p><span data-ttu-id="5837e-165"><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-165"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
<li><p><span data-ttu-id="5837e-166">Der angegebene Systemparameter ist nur pro Instanz und es wurde versucht, den globalen Wert für diesen Systemparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5837e-166">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p>
<p><span data-ttu-id="5837e-167"><strong>Windows XP und Windows Server 2003:</strong>  Dies kann nur unter Windows XP und Windows Server 2003 vorkommen.</span><span class="sxs-lookup"><span data-stu-id="5837e-167"><strong>Windows XP and Windows Server 2003:</strong>  This can only happen on Windows XP and Windows Server 2003.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-168">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="5837e-168">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="5837e-169">Der angegebene Dateisystempfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5837e-169">The specified file system path was invalid.</span></span> <span data-ttu-id="5837e-170">Dieser Fehler kann von <strong>jetsetsystemparameter</strong> nur zurückgegeben werden, wenn Systemparameter festgelegt werden, die Dateisystem Pfade darstellen.</span><span class="sxs-lookup"><span data-stu-id="5837e-170">This error may be returned by <strong>JetSetSystemParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="5837e-171">Beispielsweise kann <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> diesen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-171">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> may return this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-172">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5837e-172">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5837e-173">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5837e-173">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-174">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5837e-174">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5837e-175">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-175">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-176">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5837e-176">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5837e-177">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="5837e-177">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-178">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="5837e-178">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="5837e-179">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5837e-179">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="5837e-180">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-180">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5837e-181">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="5837e-181">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-182">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="5837e-182">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="5837e-183">Der Instanzhandle ist ungültig oder verweist auf eine Instanz, die heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="5837e-183">The instance handle is invalid or refers to an instance that has been shutdown.</span></span></p>
<p><span data-ttu-id="5837e-184">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-184">This error is not returned under all circumstances.</span></span> <span data-ttu-id="5837e-185">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="5837e-185">Handles are validated on a best effort basis only.</span></span></p>
<p><span data-ttu-id="5837e-186"><strong>Windows Vista:</strong>  Dieser Fehler wird nur von Windows Vista und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5837e-186"><strong>Windows Vista:</strong>  This error will only be returned by Windows Vista and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5837e-187">Bei Erfolg wird die Einstellung für den Systemparameter auf den angegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5837e-187">On success, the setting for the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="5837e-188">Bei einem Fehler bleibt die Einstellung für den Systemparameter unverändert.</span><span class="sxs-lookup"><span data-stu-id="5837e-188">On failure, the setting for the system parameter will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5837e-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5837e-189">Remarks</span></span>

<span data-ttu-id="5837e-190">**Jetsetsystemparameter** ist ein schlechter Auftrag der Überprüfung der ausgewählten Einstellung für jeden Systemparameter.</span><span class="sxs-lookup"><span data-stu-id="5837e-190">**JetSetSystemParameter** does a poor job of validating the chosen setting for each system parameter.</span></span> <span data-ttu-id="5837e-191">Es muss darauf geachtet werden, dass Sie sich nicht auf diese Validierung verlassen, um gute Einstellungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="5837e-191">Care must be taken to not rely on this validation to enforce good settings.</span></span> <span data-ttu-id="5837e-192">Achten Sie auf die Beschreibung der einzelnen Systemparameter, und befolgen Sie diese Richtlinien für eine gute Systemparameter Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5837e-192">Please pay close attention to the description of each system parameter and follow those guidelines for a good system parameter setting.</span></span>

<span data-ttu-id="5837e-193">Es gibt eine Reihe von Systemparametern, die immer festgelegt werden sollten, um sicherzustellen, dass die Datenbank-Engine ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5837e-193">There are a set of system parameters that should always be set to guarantee that the database engine works as intended.</span></span> <span data-ttu-id="5837e-194">Insbesondere sollten alle Systemparameter, die das physische Layout der von der Datenbank-Engine verwendeten Dateien beeinflussen, immer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5837e-194">Specifically, any system parameters that affect the physical layout of the files used by the database engine should always be set.</span></span> <span data-ttu-id="5837e-195">Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5837e-195">For more information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="5837e-196">Jeder Systemparameter verfügt über einen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="5837e-196">Every system parameter has a default value.</span></span> <span data-ttu-id="5837e-197">Diese Standardwerte wurden im Laufe der Zeit weiterentwickelt und sind beliebig.</span><span class="sxs-lookup"><span data-stu-id="5837e-197">These default values have evolved over time and are quite arbitrary.</span></span> <span data-ttu-id="5837e-198">Es wird dringend empfohlen, dass eine Anwendung alle Standardwerte auswertet, um sicherzustellen, dass Sie geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="5837e-198">It is highly recommended that an application evaluate all the default values to ensure that they are appropriate.</span></span> <span data-ttu-id="5837e-199">Wenn Sie nicht geeignet sind, sollten Sie von der Anwendung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5837e-199">If they are not appropriate, then they should be configured by the application.</span></span> <span data-ttu-id="5837e-200">Dies ist wichtig, da viele dieser Parameter die Zuverlässigkeit, Leistung und Ressourcennutzung der Datenbank-Engine erheblich beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="5837e-200">This is important as many of these parameters can greatly impact the reliability, performance, and resource utilization of the database engine.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5837e-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5837e-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5837e-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-203">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5837e-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-205">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5837e-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-207">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5837e-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-208"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-209">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5837e-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5837e-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-211">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5837e-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5837e-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5837e-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5837e-213">Implementiert als <strong>jetsetsystemparameterw</strong> (Unicode) und <strong>jetsetsystemparametera</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5837e-213">Implemented as <strong>JetSetSystemParameterW</strong> (Unicode) and <strong>JetSetSystemParameterA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5837e-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5837e-214">See Also</span></span>

[<span data-ttu-id="5837e-215">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="5837e-215">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="5837e-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5837e-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5837e-217">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5837e-217">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5837e-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5837e-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5837e-219">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="5837e-219">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="5837e-220">Jetgetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="5837e-220">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="5837e-221">JetInit</span><span class="sxs-lookup"><span data-stu-id="5837e-221">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="5837e-222">System Parameter</span><span class="sxs-lookup"><span data-stu-id="5837e-222">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
