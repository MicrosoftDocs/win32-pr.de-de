---
description: Fordert an, dass der Status des Migrations Auftrags in den angegebenen Zustand geändert wird.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: RequestStateChange-Methode der Msvm_MigrationJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356144"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="4a1c7-103">RequestStateChange-Methode der MSVM \_ migrationjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="4a1c7-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="4a1c7-104">Fordert an, dass der Status des Migrations Auftrags in den angegebenen Zustand geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="4a1c7-105">Wenn Sie die **requestStateChange** -Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben werden oder verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="4a1c7-106">Wenn 0 zurückgegeben wird, wurde der Task erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="4a1c7-107">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a1c7-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="4a1c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a1c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1c7-110">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a1c7-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a1c7-111">Der neue Status eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="4a1c7-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-113">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="4a1c7-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="4a1c7-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-115">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-115">Stops the job temporarily.</span></span> <span data-ttu-id="4a1c7-116">Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="4a1c7-117">Möglicherweise ist es möglich, den Status "Dienst" in den Status "angehalten" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="4a1c7-118">(Dies ist Auftrags spezifisch.)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="4a1c7-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-120">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und schließt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="4a1c7-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-122">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4a1c7-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-124">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="4a1c7-125">Möglicherweise ist es möglich, den Auftrag neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4a1c7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert**</span><span class="sxs-lookup"><span data-stu-id="4a1c7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4a1c7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert**</span><span class="sxs-lookup"><span data-stu-id="4a1c7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="4a1c7-129">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4a1c7-130">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a1c7-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a1c7-131">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="4a1c7-132">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="4a1c7-133">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="4a1c7-134">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (Use of Timeout Parameter not supported) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a1c7-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1c7-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a1c7-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="4a1c7-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="4a1c7-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4a1c7-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a1c7-148">Requirements</span></span>



| <span data-ttu-id="4a1c7-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a1c7-149">Requirement</span></span> | <span data-ttu-id="4a1c7-150">Wert</span><span class="sxs-lookup"><span data-stu-id="4a1c7-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1c7-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1c7-152">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a1c7-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a1c7-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a1c7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1c7-154">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a1c7-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a1c7-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a1c7-155">Namespace</span></span><br/>                | <span data-ttu-id="4a1c7-156">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a1c7-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4a1c7-157">MOF</span><span class="sxs-lookup"><span data-stu-id="4a1c7-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a1c7-158"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4a1c7-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a1c7-159">DLL</span><span class="sxs-lookup"><span data-stu-id="4a1c7-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a1c7-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a1c7-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a1c7-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a1c7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1c7-162">**MSVM \_ migrationjob**</span><span class="sxs-lookup"><span data-stu-id="4a1c7-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




