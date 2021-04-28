---
description: 'RequestStateChange-Methode der Msvm_StorageJob-Klasse: Fordert eine Zustandsänderung an.'
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: RequestStateChange-Methode der Msvm_StorageJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e15f28af892e713f8bd6897b2d75b6b227886ad1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111348"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="843ef-103">RequestStateChange-Methode der Msvm \_ StorageJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="843ef-103">RequestStateChange method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="843ef-104">Fordert eine Zustandsänderung an.</span><span class="sxs-lookup"><span data-stu-id="843ef-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="843ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="843ef-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="843ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="843ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843ef-107">*RequestedState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="843ef-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843ef-108">RequestStateChange ändert den Status eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="843ef-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="843ef-109">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="843ef-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="843ef-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="843ef-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="843ef-111">Ändert den Status in "Wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="843ef-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="843ef-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Anhalten** (3)</span><span class="sxs-lookup"><span data-stu-id="843ef-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="843ef-113">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="843ef-113">Stops the job temporarily.</span></span> <span data-ttu-id="843ef-114">Die Absicht besteht darin, den Auftrag anschließend mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="843ef-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="843ef-115">Es kann möglich sein, den Status "Dienst" zu erhalten, während er angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="843ef-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="843ef-116">(Dies ist auftragsspezifisch.)</span><span class="sxs-lookup"><span data-stu-id="843ef-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="843ef-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span><span class="sxs-lookup"><span data-stu-id="843ef-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="843ef-118">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="843ef-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="843ef-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="843ef-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="843ef-120">Beendet den Auftrag sofort, ohne dass Daten gespeichert oder der Zustand beibehalten werden muss.</span><span class="sxs-lookup"><span data-stu-id="843ef-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="843ef-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="843ef-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="843ef-122">Versetzt den Auftrag in einen anbieterspezifischen Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="843ef-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="843ef-123">Möglicherweise kann der Auftrag neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="843ef-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="843ef-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="843ef-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="843ef-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="843ef-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="843ef-126">*TimeoutPeriod* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="843ef-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843ef-127">Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="843ef-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="843ef-128">Das Intervallformat muss verwendet werden, um den Timeoutzeitraum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="843ef-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="843ef-129">Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="843ef-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="843ef-130">Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**Use Of Timeout Parameter Not Supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="843ef-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="843ef-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="843ef-131">Return value</span></span>

<span data-ttu-id="843ef-132">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="843ef-132">This method returns one of the following values:</span></span>

<dl> <dt>

 <span data-ttu-id="843ef-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="843ef-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="843ef-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="843ef-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="843ef-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="843ef-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="843ef-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="843ef-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="843ef-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="843ef-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="843ef-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="843ef-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="843ef-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="843ef-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="843ef-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="843ef-145">Requirements</span></span>



| <span data-ttu-id="843ef-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="843ef-146">Requirement</span></span> | <span data-ttu-id="843ef-147">Wert</span><span class="sxs-lookup"><span data-stu-id="843ef-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843ef-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="843ef-148">Minimum supported client</span></span><br/> | <span data-ttu-id="843ef-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="843ef-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="843ef-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="843ef-150">Minimum supported server</span></span><br/> | <span data-ttu-id="843ef-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="843ef-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="843ef-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="843ef-152">Namespace</span></span><br/>                | <span data-ttu-id="843ef-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="843ef-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="843ef-154">MOF</span><span class="sxs-lookup"><span data-stu-id="843ef-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="843ef-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="843ef-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="843ef-156">DLL</span><span class="sxs-lookup"><span data-stu-id="843ef-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="843ef-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="843ef-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="843ef-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="843ef-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843ef-159">**Msvm \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="843ef-159">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




