---
description: Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Msvm_GuestService:: requestStateChange-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757650"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="c1667-103">MSVM \_ guestservice:: requestStateChange-Methode</span><span class="sxs-lookup"><span data-stu-id="c1667-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="c1667-104">Fordert an, dass der Zustand des Gast Diensts auf den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c1667-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1667-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1667-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c1667-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1667-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1667-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1667-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="c1667-108">The new state.</span></span> <span data-ttu-id="c1667-109">Die Informationen werden in der **requestedstate** -Eigenschaft der-Instanz abgelegt, wenn der Rückgabecode der **requestStateChange** -Methode 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="c1667-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="c1667-110">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** für das-Element.</span><span class="sxs-lookup"><span data-stu-id="c1667-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="c1667-111">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="c1667-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c1667-112">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c1667-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c1667-113">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c1667-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="c1667-114">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="c1667-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="c1667-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="c1667-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="c1667-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="c1667-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="c1667-117">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="c1667-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c1667-118">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="c1667-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="c1667-119">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="c1667-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="c1667-120">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="c1667-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c1667-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c1667-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c1667-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="c1667-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c1667-123">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c1667-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1667-124">Ein optionaler Verweis auf ein CIM-" [**\_ concretejob**](cim-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1667-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="c1667-125">Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1667-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="c1667-126">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1667-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1667-127">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="c1667-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c1667-128">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1667-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="c1667-129">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="c1667-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="c1667-130">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1667-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1667-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1667-131">Return value</span></span>

<span data-ttu-id="c1667-132">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c1667-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="c1667-133">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c1667-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="c1667-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1667-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1667-135"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="c1667-136">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c1667-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="c1667-137"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="c1667-138">Über <dt>**prüfte Methoden Parameter-der Übergang**</dt> wurde <dt>4096</dt> gestartet.</span><span class="sxs-lookup"><span data-stu-id="c1667-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="c1667-139">Der Übergang erfolgt asynchron.</span><span class="sxs-lookup"><span data-stu-id="c1667-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="c1667-140"><dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="c1667-141"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="c1667-142">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c1667-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="c1667-143"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="c1667-144">Der im *requestedstate* -Parameter angegebene Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1667-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1667-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1667-145">Requirements</span></span>



| <span data-ttu-id="c1667-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1667-146">Requirement</span></span> | <span data-ttu-id="c1667-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c1667-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1667-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1667-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c1667-149">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="c1667-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c1667-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1667-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c1667-151">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1667-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c1667-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1667-152">Namespace</span></span><br/>                | <span data-ttu-id="c1667-153">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1667-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c1667-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c1667-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1667-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1667-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c1667-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1667-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1667-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1667-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1667-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1667-159">**MSVM- \_ guestservice**</span><span class="sxs-lookup"><span data-stu-id="c1667-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




