---
description: 'Weitere Informationen: Rückruf Parameter'
title: Rückruf Parameter
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130212"
---
# <a name="callback-parameters"></a><span data-ttu-id="13861-103">Rückruf Parameter</span><span class="sxs-lookup"><span data-stu-id="13861-103">Callback Parameters</span></span>


<span data-ttu-id="13861-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="13861-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="13861-105">Rückruf Parameter</span><span class="sxs-lookup"><span data-stu-id="13861-105">Callback Parameters</span></span>

<span data-ttu-id="13861-106">Dieses Thema enthält Parameter, die für Rückrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13861-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="13861-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="13861-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="13861-108">65</span><span class="sxs-lookup"><span data-stu-id="13861-108">65</span></span>  

<span data-ttu-id="13861-109">Mit diesem Parameter werden alle Datenbank-Engine-Rückrufe in von der Anwendung bereitgestellten Funktionen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="13861-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="13861-110">Es ist hauptsächlich für die Unterstützung der Datenbank-Engine-Hilfsprogramme vorgesehen und ist nicht für die Verwendung in der Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="13861-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13861-111">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="13861-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="13861-112">False</span><span class="sxs-lookup"><span data-stu-id="13861-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="13861-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="13861-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="13861-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-115">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="13861-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="13861-116">False, True</span><span class="sxs-lookup"><span data-stu-id="13861-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-117">Umfang:</span><span class="sxs-lookup"><span data-stu-id="13861-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="13861-118">Instanz</span><span class="sxs-lookup"><span data-stu-id="13861-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-119">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-120">Ja</span><span class="sxs-lookup"><span data-stu-id="13861-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-121">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-122">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-123">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="13861-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="13861-124">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-125">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="13861-126">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-127">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="13861-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="13861-128">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-129">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="13861-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="13861-130">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-131">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="13861-132">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="13861-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13861-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="13861-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="13861-134">156</span><span class="sxs-lookup"><span data-stu-id="13861-134">156</span></span>  

<span data-ttu-id="13861-135">Dieser Parameter ermöglicht die Verwendung persistenter Rückrufe in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="13861-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="13861-136">In Releases vor Windows Vista war die Verwendung persistenter Rückrufe standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="13861-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="13861-137">Anwendungen müssen nun mithilfe dieses Parameters die Verwendung von permanenten Rückrufen zur Laufzeit explizit aktivieren.</span><span class="sxs-lookup"><span data-stu-id="13861-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="13861-138">Wenn dieser Parameter nicht festgelegt ist, schlägt jeder Daten Bank Vorgang, der den Aufruf eines Rückrufs erfordert, mit JET_errCallbackFailed fehl.</span><span class="sxs-lookup"><span data-stu-id="13861-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="13861-139">Dieser Parameter hat keine Auswirkung auf Rückrufe, die zur Laufzeit mit den folgenden Mechanismen angegeben werden: JET_paramRuntimeCallback, [jetregistercallback](./jetregistercallback-function.md)oder ein expliziter Rückruf Parameter für eine Jet-API.</span><span class="sxs-lookup"><span data-stu-id="13861-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="13861-140">Es ist immer noch möglich, Schema Elemente zu erstellen, die persistente Rückrufe enthalten, auch wenn die Verwendung dieser permanenten Rückrufe nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="13861-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="13861-141">Wenn dieser Parameter auf false festgelegt ist, überschreibt er JET_paramDisableCallbacks.</span><span class="sxs-lookup"><span data-stu-id="13861-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13861-142">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="13861-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="13861-143">False</span><span class="sxs-lookup"><span data-stu-id="13861-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-144">Typ:</span><span class="sxs-lookup"><span data-stu-id="13861-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="13861-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="13861-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-146">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="13861-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="13861-147">False, True</span><span class="sxs-lookup"><span data-stu-id="13861-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-148">Umfang:</span><span class="sxs-lookup"><span data-stu-id="13861-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="13861-149">Instanz</span><span class="sxs-lookup"><span data-stu-id="13861-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-150">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-151">Ja</span><span class="sxs-lookup"><span data-stu-id="13861-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-152">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-153">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-154">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="13861-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="13861-155">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-156">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="13861-157">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-158">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="13861-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="13861-159">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-160">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="13861-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="13861-161">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-162">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="13861-163">Windows Vista und spätere Versionen</span><span class="sxs-lookup"><span data-stu-id="13861-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="13861-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="13861-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="13861-165">73</span><span class="sxs-lookup"><span data-stu-id="13861-165">73</span></span>  

<span data-ttu-id="13861-166">Dieser Parameter konfiguriert die-Engine mit einer Lauf Zeit Rückruffunktion, die die [JET_CALLBACK](./jet-callback-callback-function.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="13861-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="13861-167">Dieser Rückruf kann aus folgenden Gründen aufgerufen werden: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)oder [JET_cbtypNull](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="13861-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="13861-168">Weitere Informationen finden Sie unter [jetsetls](./jetsetls-function.md) .</span><span class="sxs-lookup"><span data-stu-id="13861-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13861-169">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="13861-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="13861-170">NULL</span><span class="sxs-lookup"><span data-stu-id="13861-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-171">Typ:</span><span class="sxs-lookup"><span data-stu-id="13861-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="13861-172">Funktionszeiger (JET_API_PTR)</span><span class="sxs-lookup"><span data-stu-id="13861-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-173">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="13861-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="13861-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="13861-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-175">Umfang:</span><span class="sxs-lookup"><span data-stu-id="13861-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="13861-176">Instanz</span><span class="sxs-lookup"><span data-stu-id="13861-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-177">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-178">Ja</span><span class="sxs-lookup"><span data-stu-id="13861-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-179">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13861-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="13861-180">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-181">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="13861-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="13861-182">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-183">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="13861-184">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-185">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="13861-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="13861-186">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-187">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="13861-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="13861-188">Nein</span><span class="sxs-lookup"><span data-stu-id="13861-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-189">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="13861-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="13861-190">Versionen von Windows XP und höher</span><span class="sxs-lookup"><span data-stu-id="13861-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="13861-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13861-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13861-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="13861-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="13861-193">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13861-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13861-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="13861-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="13861-195">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="13861-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13861-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="13861-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="13861-197">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="13861-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="13861-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13861-198">See Also</span></span>

[<span data-ttu-id="13861-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="13861-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="13861-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="13861-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="13861-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="13861-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="13861-202">Jetkreateingestance</span><span class="sxs-lookup"><span data-stu-id="13861-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="13861-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="13861-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="13861-204">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="13861-204">JetSetLS</span></span>](./jetsetls-function.md)
