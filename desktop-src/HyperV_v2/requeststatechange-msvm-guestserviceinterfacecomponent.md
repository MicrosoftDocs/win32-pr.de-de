---
description: Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Msvm_GuestServiceInterfaceComponent:: requestStateChange-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362454"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="60856-103">MSVM \_ guestserviceinterfacecomponent:: requestStateChange-Methode</span><span class="sxs-lookup"><span data-stu-id="60856-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="60856-104">Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="60856-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60856-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60856-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="60856-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60856-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60856-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60856-108">Typ: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60856-108">Type: **uint16**</span></span>

<span data-ttu-id="60856-109">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="60856-109">The new state.</span></span> <span data-ttu-id="60856-110">Die Informationen werden in der **requestedstate** -Eigenschaft der-Instanz abgelegt, wenn der Rückgabecode der **requestStateChange** -Methode 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="60856-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="60856-111">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** für das-Element.</span><span class="sxs-lookup"><span data-stu-id="60856-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="60856-112">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="60856-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="60856-113">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="60856-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="60856-114">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="60856-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="60856-115">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="60856-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="60856-116">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="60856-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="60856-117">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="60856-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="60856-118">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="60856-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="60856-119">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="60856-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="60856-120">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="60856-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="60856-121">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="60856-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60856-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60856-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="60856-123">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="60856-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="60856-124">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="60856-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60856-125">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="60856-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="60856-126">Ein optionaler Verweis auf ein [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Objekt, das zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60856-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="60856-127">Falls vorhanden, kann der zurückgegebene Verweis zum Überwachen des Fortschritts und zum Abrufen des Ergebnisses der Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60856-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="60856-128">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60856-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60856-129">Type: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60856-129">Type: **datetime**</span></span>

<span data-ttu-id="60856-130">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="60856-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="60856-131">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60856-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="60856-132">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="60856-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="60856-133">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60856-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60856-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60856-134">Return value</span></span>

<span data-ttu-id="60856-135">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60856-135">Type: **uint32**</span></span>

<span data-ttu-id="60856-136">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="60856-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="60856-137">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="60856-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="60856-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60856-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="60856-139"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60856-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="60856-140">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="60856-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="60856-141"><dt>**Nicht unterstützt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="60856-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="60856-142"><dt>**Unbekannter/nicht**</dt> angegebener Fehler <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="60856-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="60856-143"><dt>**Kann nicht innerhalb des Timeout Zeitraums**</dt> <dt>3</dt> beendet werden.</span><span class="sxs-lookup"><span data-stu-id="60856-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="60856-144"><dt></dt> Fehler <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="60856-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="60856-145"><dt>**Ungültiger Parameter**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="60856-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="60856-146"><dt>**In Verwendung**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="60856-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="60856-147"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="60856-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="60856-148">Über <dt>**prüfte Methoden Parameter-der Übergang**</dt> wurde <dt>4096</dt> gestartet.</span><span class="sxs-lookup"><span data-stu-id="60856-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="60856-149"><dt>**Ungültiger Status Übergang**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="60856-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="60856-150"><dt>**Verwendung des timeout-Parameters wird nicht unterstützt**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="60856-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="60856-151"><dt>**Ausgelastet**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="60856-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="60856-152"><dt>**Methode reserviert**</dt> <dt>4100.32767</dt></span><span class="sxs-lookup"><span data-stu-id="60856-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="60856-153"><dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="60856-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="60856-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60856-154">Requirements</span></span>



| <span data-ttu-id="60856-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60856-155">Requirement</span></span> | <span data-ttu-id="60856-156">Wert</span><span class="sxs-lookup"><span data-stu-id="60856-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60856-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60856-157">Minimum supported client</span></span><br/> | <span data-ttu-id="60856-158">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="60856-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="60856-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60856-159">Minimum supported server</span></span><br/> | <span data-ttu-id="60856-160">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60856-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60856-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="60856-161">Namespace</span></span><br/>                | <span data-ttu-id="60856-162">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="60856-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="60856-163">MOF</span><span class="sxs-lookup"><span data-stu-id="60856-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60856-164"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60856-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60856-165">DLL</span><span class="sxs-lookup"><span data-stu-id="60856-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60856-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60856-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60856-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60856-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60856-168">**MSVM \_ guestserviczuterfacecomponent**</span><span class="sxs-lookup"><span data-stu-id="60856-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

