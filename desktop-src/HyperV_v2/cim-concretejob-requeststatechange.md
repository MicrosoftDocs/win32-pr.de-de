---
description: Fordert an, dass der Status des Auftrags in den im requestedstate-Parameter angegebenen Wert geändert wird. Wenn Sie die requestStateChange-Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben oder verloren gehen.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: RequestStateChange-Methode der CIM_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344129"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="90129-104">RequestStateChange-Methode der CIM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="90129-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="90129-105">Fordert an, dass der Status des Auftrags in den im requestedstate-Parameter angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="90129-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="90129-106">Wenn Sie die requestStateChange-Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben oder verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="90129-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="90129-107">Wenn 0 zurückgegeben wird, wurde der Task erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="90129-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="90129-108">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="90129-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="90129-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="90129-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="90129-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90129-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90129-111">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90129-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90129-112">Der Status, der für einen Auftrag angefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90129-112">The state to request for a job.</span></span> <span data-ttu-id="90129-113">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="90129-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="90129-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="90129-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="90129-115">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="90129-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="90129-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="90129-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="90129-117">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="90129-117">Stops the job temporarily.</span></span> <span data-ttu-id="90129-118">Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="90129-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="90129-119">Möglicherweise ist es möglich, den Zustand "Dienst" in den Status "angehalten" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="90129-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="90129-120">(Dies ist Auftrags spezifisch.)</span><span class="sxs-lookup"><span data-stu-id="90129-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="90129-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="90129-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="90129-122">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="90129-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="90129-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="90129-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="90129-124">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="90129-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="90129-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="90129-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="90129-126">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="90129-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="90129-127">Möglicherweise ist es möglich, den Auftrag neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="90129-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="90129-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="90129-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="90129-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="90129-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="90129-130">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90129-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90129-131">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="90129-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="90129-132">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90129-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="90129-133">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="90129-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="90129-134">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90129-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90129-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90129-135">Return value</span></span>

<span data-ttu-id="90129-136">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90129-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="90129-137">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="90129-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90129-138">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="90129-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="90129-139">**Unbekannter/nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="90129-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="90129-140">**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="90129-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="90129-141">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="90129-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="90129-142">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="90129-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="90129-143">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="90129-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="90129-144">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="90129-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="90129-145">Über **prüfte Methoden Parameter-der Übergang wurde gestartet** (4096).</span><span class="sxs-lookup"><span data-stu-id="90129-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="90129-146">**Ungültiger Status Übergang** (4097).</span><span class="sxs-lookup"><span data-stu-id="90129-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="90129-147">**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)</span><span class="sxs-lookup"><span data-stu-id="90129-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="90129-148">**Ausgelastet** (4099)</span><span class="sxs-lookup"><span data-stu-id="90129-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="90129-149">**Reservierte Methode** (4100.32767)</span><span class="sxs-lookup"><span data-stu-id="90129-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="90129-150">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="90129-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90129-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90129-151">Requirements</span></span>



| <span data-ttu-id="90129-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90129-152">Requirement</span></span> | <span data-ttu-id="90129-153">Wert</span><span class="sxs-lookup"><span data-stu-id="90129-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90129-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90129-154">Minimum supported client</span></span><br/> | <span data-ttu-id="90129-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="90129-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="90129-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90129-156">Minimum supported server</span></span><br/> | <span data-ttu-id="90129-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="90129-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="90129-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="90129-158">Namespace</span></span><br/>                | <span data-ttu-id="90129-159">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="90129-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90129-160">MOF</span><span class="sxs-lookup"><span data-stu-id="90129-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90129-161"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90129-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90129-162">DLL</span><span class="sxs-lookup"><span data-stu-id="90129-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90129-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90129-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90129-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90129-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90129-165">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="90129-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




