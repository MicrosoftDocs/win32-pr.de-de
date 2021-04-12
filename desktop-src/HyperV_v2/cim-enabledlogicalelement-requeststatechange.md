---
description: Fordert an, dass der Zustand des Elements in den im requestedstate-Parameter angegebenen Wert geändert wird.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: RequestStateChange-Methode der CIM_EnabledLogicalElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345798"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="34f84-103">RequestStateChange-Methode der CIM \_ enabledlogicalelement-Klasse</span><span class="sxs-lookup"><span data-stu-id="34f84-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="34f84-104">Fordert an, dass der Zustand des Elements in den im requestedstate-Parameter angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="34f84-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="34f84-105">Wenn die angeforderte Zustandsänderung stattfindet, sind enabledstate und requestedstate des Elements identisch.</span><span class="sxs-lookup"><span data-stu-id="34f84-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="34f84-106">Wenn Sie die requestStateChange-Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben oder verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="34f84-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="34f84-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="34f84-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34f84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f84-109">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34f84-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f84-110">Der für das Element angeforderte Zustand.</span><span class="sxs-lookup"><span data-stu-id="34f84-110">The state requested for the element.</span></span> <span data-ttu-id="34f84-111">Diese Informationen werden in die **requestedstate** -Eigenschaft der-Instanz eingefügt, wenn der Rückgabecode der **requestStateChange** -Methode 0 (' abgeschlossen ohne Fehler ') oder 4096 (0x1000) (' Auftrag gestartet ') ist.</span><span class="sxs-lookup"><span data-stu-id="34f84-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="34f84-112">Ausführliche Erläuterungen zu den **requestedstate** -Werten finden Sie in der Beschreibung der Eigenschaften " **enabledstate** " und " **requestedstate** ".</span><span class="sxs-lookup"><span data-stu-id="34f84-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="34f84-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="34f84-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="34f84-114">Ändert den Zustand in "wird ausgeführt".</span><span class="sxs-lookup"><span data-stu-id="34f84-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="34f84-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Aussetzen** (3)</span><span class="sxs-lookup"><span data-stu-id="34f84-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="34f84-116">Beendet den Auftrag vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="34f84-116">Stops the job temporarily.</span></span> <span data-ttu-id="34f84-117">Die Absicht besteht darin, den Auftrag mit "Start" neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="34f84-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="34f84-118">Möglicherweise ist es möglich, den Zustand "Dienst" in den Status "angehalten" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="34f84-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="34f84-119">(Dies ist Auftrags spezifisch.)</span><span class="sxs-lookup"><span data-stu-id="34f84-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="34f84-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (4)</span><span class="sxs-lookup"><span data-stu-id="34f84-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="34f84-121">Beendet den Auftrag ordnungsgemäß, speichert Daten, behält den Zustand bei und fährt alle zugrunde liegenden Prozesse ordnungsgemäß herunter.</span><span class="sxs-lookup"><span data-stu-id="34f84-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="34f84-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="34f84-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="34f84-123">Beendet den Auftrag sofort, ohne dass es erforderlich ist, Daten zu speichern oder den Zustand beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="34f84-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="34f84-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Dienst** (6)</span><span class="sxs-lookup"><span data-stu-id="34f84-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="34f84-125">Versetzt den Auftrag in einen herstellerspezifischen Dienst Zustand.</span><span class="sxs-lookup"><span data-stu-id="34f84-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="34f84-126">Möglicherweise ist es möglich, den Auftrag neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="34f84-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="34f84-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="34f84-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="34f84-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="34f84-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="34f84-129">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="34f84-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34f84-130">Kann einen Verweis auf den erstellten [**CIM- \_ bettejob**](cim-concretejob.md) enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="34f84-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="34f84-131">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34f84-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f84-132">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="34f84-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="34f84-133">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34f84-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="34f84-134">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="34f84-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="34f84-135">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34f84-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f84-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34f84-136">Return value</span></span>

<span data-ttu-id="34f84-137">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34f84-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="34f84-138">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="34f84-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-139">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="34f84-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-140">**Unbekannter oder nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="34f84-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-141">**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="34f84-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-142">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="34f84-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-143">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="34f84-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-144">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="34f84-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-145">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="34f84-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-146">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="34f84-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-147">**Ungültiger Status Übergang** (4097).</span><span class="sxs-lookup"><span data-stu-id="34f84-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-148">**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)</span><span class="sxs-lookup"><span data-stu-id="34f84-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-149">**Ausgelastet** (4099)</span><span class="sxs-lookup"><span data-stu-id="34f84-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-150">**Reservierte Methode** (4100.32767)</span><span class="sxs-lookup"><span data-stu-id="34f84-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="34f84-151">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="34f84-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="34f84-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f84-152">Requirements</span></span>



| <span data-ttu-id="34f84-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f84-153">Requirement</span></span> | <span data-ttu-id="34f84-154">Wert</span><span class="sxs-lookup"><span data-stu-id="34f84-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f84-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34f84-155">Minimum supported client</span></span><br/> | <span data-ttu-id="34f84-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="34f84-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="34f84-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34f84-157">Minimum supported server</span></span><br/> | <span data-ttu-id="34f84-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="34f84-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="34f84-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="34f84-159">Namespace</span></span><br/>                | <span data-ttu-id="34f84-160">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="34f84-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="34f84-161">MOF</span><span class="sxs-lookup"><span data-stu-id="34f84-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34f84-162"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34f84-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34f84-163">DLL</span><span class="sxs-lookup"><span data-stu-id="34f84-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34f84-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34f84-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34f84-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34f84-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f84-166">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="34f84-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 




