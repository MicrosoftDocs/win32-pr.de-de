---
description: Ändert den Status des Auftrags.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob:: requestStateChange-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349947"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="f1ae2-103">MSVM \_ copyfiletoguestjob:: requestStateChange-Methode</span><span class="sxs-lookup"><span data-stu-id="f1ae2-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="f1ae2-104">Ändert den Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ae2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1ae2-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f1ae2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ae2-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1ae2-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ae2-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-108">The new state.</span></span> <span data-ttu-id="f1ae2-109">Dies sind die möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="f1ae2-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="f1ae2-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f1ae2-111">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="f1ae2-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f1ae2-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1ae2-113">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-113">Stops the job temporarily.</span></span> <span data-ttu-id="f1ae2-114">Anschließend kann der Client den Auftrag mit "Start" neu starten.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="f1ae2-115">Der Client kann möglicherweise den Zustand "Dienst" eingeben, während er angehalten wird (Dies ist Auftrags spezifisch).</span><span class="sxs-lookup"><span data-stu-id="f1ae2-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="f1ae2-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1ae2-117">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und schließt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="f1ae2-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f1ae2-119">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1ae2-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1ae2-121">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="f1ae2-122">Der Client kann den Auftrag möglicherweise neu starten.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f1ae2-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f1ae2-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f1ae2-125">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1ae2-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ae2-126">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f1ae2-127">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f1ae2-128">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f1ae2-129">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ae2-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1ae2-130">Return value</span></span>

<span data-ttu-id="f1ae2-131">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="f1ae2-132">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f1ae2-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="f1ae2-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1ae2-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1ae2-134"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="f1ae2-135">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="f1ae2-136"><dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-137"><dt></dt> Fehler <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-138"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="f1ae2-139">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="f1ae2-140"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-141"><dt>**Status ist unbekannt**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-142"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-143"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-144"><dt>**System wird verwendet**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-145"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="f1ae2-146">Der im *requestedstate* -Parameter angegebene Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="f1ae2-147"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-148"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="f1ae2-149"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="f1ae2-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1ae2-150">Requirements</span></span>



| <span data-ttu-id="f1ae2-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1ae2-151">Requirement</span></span> | <span data-ttu-id="f1ae2-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f1ae2-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ae2-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ae2-154">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f1ae2-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f1ae2-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1ae2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ae2-156">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1ae2-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f1ae2-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1ae2-157">Namespace</span></span><br/>                | <span data-ttu-id="f1ae2-158">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1ae2-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="f1ae2-159">MOF</span><span class="sxs-lookup"><span data-stu-id="f1ae2-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1ae2-160"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1ae2-161">DLL</span><span class="sxs-lookup"><span data-stu-id="f1ae2-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1ae2-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1ae2-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1ae2-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1ae2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ae2-164">**MSVM \_ copyfilein guestjob**</span><span class="sxs-lookup"><span data-stu-id="f1ae2-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




