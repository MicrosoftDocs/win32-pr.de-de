---
description: Fordert eine Statusänderung an.
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: RequestStateChange-Methode der Msvm_VirtualSystemReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354914"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="e189a-103">RequestStateChange-Methode der MSVM \_ virtualsystemreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="e189a-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="e189a-104">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="e189a-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="e189a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e189a-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="e189a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e189a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e189a-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e189a-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e189a-108">Ändert den Zustand eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="e189a-108">Changes the state of a job.</span></span> <span data-ttu-id="e189a-109">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e189a-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="e189a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="e189a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e189a-111">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="e189a-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="e189a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="e189a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e189a-113">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="e189a-113">Stops the job temporarily.</span></span> <span data-ttu-id="e189a-114">Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e189a-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="e189a-115">Möglicherweise ist es möglich, den Zustand "Dienst" in den Status "angehalten" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="e189a-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="e189a-116">(Dies ist Auftrags spezifisch.)</span><span class="sxs-lookup"><span data-stu-id="e189a-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="e189a-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="e189a-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e189a-118">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="e189a-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="e189a-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="e189a-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e189a-120">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e189a-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e189a-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="e189a-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e189a-122">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="e189a-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="e189a-123">Möglicherweise ist es möglich, den Auftrag neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e189a-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e189a-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e189a-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e189a-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="e189a-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e189a-126">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e189a-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e189a-127">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="e189a-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="e189a-128">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e189a-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="e189a-129">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="e189a-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="e189a-130">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e189a-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e189a-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e189a-131">Return value</span></span>

<span data-ttu-id="e189a-132">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e189a-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="e189a-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="e189a-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="e189a-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="e189a-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="e189a-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="e189a-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="e189a-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="e189a-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="e189a-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="e189a-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="e189a-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="e189a-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="e189a-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="e189a-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e189a-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e189a-145">Requirements</span></span>



| <span data-ttu-id="e189a-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e189a-146">Requirement</span></span> | <span data-ttu-id="e189a-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e189a-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e189a-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e189a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e189a-149">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e189a-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e189a-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e189a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e189a-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e189a-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e189a-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="e189a-152">Namespace</span></span><br/>                | <span data-ttu-id="e189a-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e189a-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e189a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e189a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e189a-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e189a-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e189a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e189a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e189a-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e189a-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e189a-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e189a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e189a-159">**MSVM \_ virtualsystemreferencepointexportjob**</span><span class="sxs-lookup"><span data-stu-id="e189a-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




