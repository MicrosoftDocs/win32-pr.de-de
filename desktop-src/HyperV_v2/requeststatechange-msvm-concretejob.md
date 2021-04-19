---
description: Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: RequestStateChange-Methode der Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359006"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="2e909-103">RequestStateChange-Methode der MSVM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="2e909-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="2e909-104">Fordert an, dass der Status des Auftrags in den angegebenen Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2e909-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="2e909-105">Wenn Sie die **requestStateChange** -Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben werden oder verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="2e909-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="2e909-106">Wenn 0 zurückgegeben wird, wurde der Task erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2e909-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="2e909-107">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="2e909-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e909-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e909-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2e909-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e909-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e909-110">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e909-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e909-111">Typ: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e909-111">Type: **uint16**</span></span>

<span data-ttu-id="2e909-112">Der neue Status eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="2e909-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="2e909-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="2e909-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e909-114">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="2e909-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="2e909-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="2e909-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e909-116">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="2e909-116">Stops the job temporarily.</span></span> <span data-ttu-id="2e909-117">Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="2e909-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="2e909-118">Möglicherweise ist es möglich, den Status "Dienst" in den Status "angehalten" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="2e909-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="2e909-119">(Dies ist Auftrags spezifisch.)</span><span class="sxs-lookup"><span data-stu-id="2e909-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="2e909-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="2e909-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e909-121">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und schließt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="2e909-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="2e909-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="2e909-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e909-123">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="2e909-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2e909-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="2e909-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e909-125">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="2e909-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="2e909-126">Möglicherweise ist es möglich, den Auftrag neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="2e909-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2e909-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert**</span><span class="sxs-lookup"><span data-stu-id="2e909-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="2e909-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="2e909-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2e909-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert**</span><span class="sxs-lookup"><span data-stu-id="2e909-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="2e909-130">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="2e909-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2e909-131">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e909-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e909-132">Type: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e909-132">Type: **datetime**</span></span>

<span data-ttu-id="2e909-133">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="2e909-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="2e909-134">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e909-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="2e909-135">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="2e909-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="2e909-136">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (Use of Timeout Parameter not supported) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2e909-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e909-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e909-137">Return value</span></span>

<span data-ttu-id="2e909-138">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e909-138">Type: **uint32**</span></span>

<span data-ttu-id="2e909-139">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2e909-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2e909-140">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2e909-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-141">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2e909-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-142">**Unbekannter/nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="2e909-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-143">**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e909-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-144">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="2e909-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-145">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="2e909-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-146">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="2e909-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-147">**DMTF reserviert** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="2e909-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-148">Über **prüfte Methoden Parameter-der Übergang wurde gestartet** (4096).</span><span class="sxs-lookup"><span data-stu-id="2e909-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-149">**Ungültiger Status Übergang** (4097).</span><span class="sxs-lookup"><span data-stu-id="2e909-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-150">**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)</span><span class="sxs-lookup"><span data-stu-id="2e909-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-151">**Ausgelastet** (4099)</span><span class="sxs-lookup"><span data-stu-id="2e909-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-152">**Reservierte Methode** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="2e909-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="2e909-153">**Hersteller spezifisch** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="2e909-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2e909-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e909-154">Remarks</span></span>

<span data-ttu-id="2e909-155">Der Zugriff auf die [**MSVM-Klasse " \_ concretejob**](msvm-concretejob.md) " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="2e909-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2e909-156">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2e909-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e909-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e909-157">Requirements</span></span>



| <span data-ttu-id="2e909-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e909-158">Requirement</span></span> | <span data-ttu-id="2e909-159">Wert</span><span class="sxs-lookup"><span data-stu-id="2e909-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e909-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e909-160">Minimum supported client</span></span><br/> | <span data-ttu-id="2e909-161">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e909-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e909-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e909-162">Minimum supported server</span></span><br/> | <span data-ttu-id="2e909-163">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e909-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e909-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e909-164">Namespace</span></span><br/>                | <span data-ttu-id="2e909-165">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e909-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e909-166">MOF</span><span class="sxs-lookup"><span data-stu-id="2e909-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e909-167"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e909-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e909-168">DLL</span><span class="sxs-lookup"><span data-stu-id="2e909-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e909-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e909-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e909-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e909-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e909-171">**MSVM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="2e909-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

