---
description: 'Weitere Informationen finden Sie hier: JetStopServiceInstance2-Funktion'
title: JetStopServiceInstance2-Funktion
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752280"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="a22ea-103">JetStopServiceInstance2-Funktion</span><span class="sxs-lookup"><span data-stu-id="a22ea-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="a22ea-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a22ea-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="a22ea-105">Die **JetStopServiceInstance2** -Funktion bereitet eine Instanz vor dem aussetzen vor und bereitet eine Instanz nach der Wiederaufnahme vor.</span><span class="sxs-lookup"><span data-stu-id="a22ea-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="a22ea-106">Suspend und Resume sind Ausführungs Zustände des Lebenszyklus Modells der Windows Store-App.</span><span class="sxs-lookup"><span data-stu-id="a22ea-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="a22ea-107">Die **JetStopServiceInstance2** -Funktion wurde in Windows 8 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a22ea-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a22ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a22ea-108">Parameters</span></span>

<span data-ttu-id="a22ea-109">*lichen*</span><span class="sxs-lookup"><span data-stu-id="a22ea-109">*instance*</span></span>

<span data-ttu-id="a22ea-110">Die Ziel Instanz.</span><span class="sxs-lookup"><span data-stu-id="a22ea-110">The target instance.</span></span> <span data-ttu-id="a22ea-111">Der **JET_INSTANCE** -Datentyp ist ein Handle für die Instanz der-Datenbank, die für einen aufzurufenden Jet-API-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a22ea-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="a22ea-112">Dieses Handle wird abgerufen, wenn Sie eine Instanz der Datenbank erstellen, indem Sie die [jetcreateinstance](./jetcreateinstance-function.md)-, [JetCreateInstance2](./jetcreateinstance2-function.md)-, [jetinit](./jetinit-function.md)-oder [JetInit2](./jetinit2-function.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a22ea-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="a22ea-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a22ea-113">*grbit*</span></span>

<span data-ttu-id="a22ea-114">Eine Gruppe von Bits, die einen oder mehrere der Werte angibt, die in der folgenden Tabelle aufgelistet und definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a22ea-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a22ea-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a22ea-115">Value</span></span></p></th>
<th><p><span data-ttu-id="a22ea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a22ea-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="a22ea-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="a22ea-118">Beendet alle ESE-Dienste (Extensible Storage Engine) für die angegebene-Instanz.</span><span class="sxs-lookup"><span data-stu-id="a22ea-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a22ea-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="a22ea-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="a22ea-120">Beendet neu startbare, vom Client angegebene Hintergrund Wartungs Tasks (z. B. B +-Struktur Defragmentierung).</span><span class="sxs-lookup"><span data-stu-id="a22ea-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="a22ea-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="a22ea-122">Versetzt alle Dirty Caches auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a22ea-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="a22ea-123">Dieser Wert ist asynchron und kann abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="a22ea-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a22ea-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="a22ea-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="a22ea-125">Setzt zuvor ausgestellte Stopp Dienst Vorgänge fort. Das heißt, dass der Dienst neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a22ea-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="a22ea-126">Dieser Wert kann mit dem <em>grbits</em> -Parameter kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit JET_bitStopServiceAll, um alle zuvor beendeten Dienste wieder aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a22ea-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="a22ea-127">Dieses Bit kann nur zum Fortsetzen von stopservicebackgroundusertasks und JET_bitStopServiceQuiesceCaches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a22ea-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="a22ea-128">Wenn Sie zuvor mit JET_bitStopServiceAll aufgerufen haben, tritt beim Versuch, JET_bitStopServiceResume zu verwenden, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a22ea-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="a22ea-129">Wenn der zweite Fortschritt nicht aufgerufen wird, wird die Leistung der Anwendung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="a22ea-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="a22ea-130">In dieser Situation wird der Prüfpunkt auf 0 (null) beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a22ea-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a22ea-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a22ea-131">Return value</span></span>

<span data-ttu-id="a22ea-132">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a22ea-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="a22ea-133">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a22ea-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a22ea-134">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a22ea-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="a22ea-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a22ea-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a22ea-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a22ea-137">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a22ea-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="a22ea-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a22ea-138">Remarks</span></span>

<span data-ttu-id="a22ea-139">Diese Funktion ermöglicht es einer Jet-Anwendung, den Daten Bank Cache in den Zustand "bereinigt" oder "fast Clean" (mit dem Betriebssystem-e/a-Leerlauf) zu verschieben, sodass die Wiederherstellung schnell ausgeführt werden kann, wenn die Anwendung beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a22ea-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="a22ea-140">Diese Vorgehensweise wird für das Beenden von Jet bevorzugt, indem die [jetterm](./jetterm-function.md) -Funktion oder die [jetdetachdatabase](./jetdetachdatabase-function.md) -Funktion aufgerufen wird, sodass die Anwendung im gängigeren Szenario nicht angehalten wird und die Anwendung später den gesamten Cache hat und so schnell wie möglich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a22ea-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="a22ea-141">Wenn diese Funktion erfolgreich ausgeführt wird, bereitet Sie den Daten Bank Cache auf eine bevorstehende Unterbrechung vor.</span><span class="sxs-lookup"><span data-stu-id="a22ea-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="a22ea-142">Diese Funktion fügt arbeiten an einen Hintergrund Arbeitsthread an und kehrt sofort an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="a22ea-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="a22ea-143">Die-Funktion sollte basierend auf dem PLM visibilitynotice aufgerufen werden, anstatt vom Handler für die Unterbrechung der Anwendung aufgerufen zu werden, um sicherzustellen, dass Jet Zeit zum leeren von Änderungs Puffern hat, bevor der Prozess von PLM angehalten oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a22ea-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="a22ea-144">Intern löst Jet eine sofortige Verteilung der Prüf Punkt Wartung bei der Konfigurationsänderung aus (entweder Checkpoint Update oder this New versetzen Caches Bit).</span><span class="sxs-lookup"><span data-stu-id="a22ea-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="a22ea-145">Weitere Informationen zu visibilitynotice-Ereignissen finden Sie unter [visibilitychangedeventargs-Klasse](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="a22ea-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="a22ea-146">Diese Funktion muss zweimal aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a22ea-146">This function must be called twice.</span></span> <span data-ttu-id="a22ea-147">Sie wird aufgerufen, nachdem die Anwendung den Suspensions Hinweis vom Betriebssystem empfangen hat, aber bevor die Anwendung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="a22ea-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="a22ea-148">Anschließend wird Sie erneut aufgerufen, nachdem das Betriebssystem die Anwendung wieder aufnimmt.</span><span class="sxs-lookup"><span data-stu-id="a22ea-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="a22ea-149">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a22ea-149">For example:</span></span>

<span data-ttu-id="a22ea-150">Beim Aufrufen zum aussetzen: JET_ERR JET_API JetStopServiceInstance2 (Instanz, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="a22ea-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="a22ea-151">Beim fortsetzen: JET_ERR JET_API JetStopServiceInstance2 (Instanz, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="a22ea-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="a22ea-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a22ea-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a22ea-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a22ea-154">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a22ea-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a22ea-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a22ea-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a22ea-156">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a22ea-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a22ea-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a22ea-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a22ea-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a22ea-159"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a22ea-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a22ea-160">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a22ea-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a22ea-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a22ea-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a22ea-162">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a22ea-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a22ea-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22ea-163">See also</span></span>

[<span data-ttu-id="a22ea-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a22ea-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a22ea-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a22ea-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a22ea-166">Jetclosedatabase</span><span class="sxs-lookup"><span data-stu-id="a22ea-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="a22ea-167">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="a22ea-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a22ea-168">Jetdetachdatabase</span><span class="sxs-lookup"><span data-stu-id="a22ea-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="a22ea-169">Jetendsession</span><span class="sxs-lookup"><span data-stu-id="a22ea-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="a22ea-170">Jetresessioncontext</span><span class="sxs-lookup"><span data-stu-id="a22ea-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="a22ea-171">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="a22ea-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a22ea-172">Jetterm</span><span class="sxs-lookup"><span data-stu-id="a22ea-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="a22ea-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="a22ea-173">JetTerm2</span></span>](./jetterm2-function.md)
