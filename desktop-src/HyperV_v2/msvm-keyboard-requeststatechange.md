---
description: Fordert an, dass der Zustand des Elements geändert wird.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: RequestStateChange-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959036"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="847a1-103">RequestStateChange-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="847a1-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="847a1-104">Fordert an, dass der Zustand des Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="847a1-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="847a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="847a1-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="847a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="847a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="847a1-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a1-108">Der für das Element angeforderte neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="847a1-108">The new state requested for the element.</span></span> <span data-ttu-id="847a1-109">Diese Informationen werden in die **requestedstate** -Eigenschaft der-Instanz eingefügt, wenn der Rückgabecode 0 (' abgeschlossen ohne Fehler '), 3 (' Timeout ') oder 4096 (0x1000) (' Auftrag gestartet ') ist.</span><span class="sxs-lookup"><span data-stu-id="847a1-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="847a1-110">Ausführliche Erläuterungen zu den *requestedstate* -Werten finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="847a1-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="847a1-111">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="847a1-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="847a1-112">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="847a1-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="847a1-113">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="847a1-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="847a1-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="847a1-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="847a1-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="847a1-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="847a1-116">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="847a1-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="847a1-117">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="847a1-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="847a1-118">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="847a1-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="847a1-119">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="847a1-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="847a1-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="847a1-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="847a1-121">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="847a1-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="847a1-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="847a1-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="847a1-123">Ein Verweis auf den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="847a1-123">A reference to the job.</span></span> <span data-ttu-id="847a1-124">Dieser Parameter kann **null** sein, wenn die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="847a1-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="847a1-125">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a1-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a1-126">Die maximale Zeitspanne, für die der Client den Übergang zum neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="847a1-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="847a1-127">Zum Angeben dieses Timeout Zeitraums muss das Intervall Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="847a1-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="847a1-128">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="847a1-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="847a1-129">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, wird der Rückgabecode 4098 ("Use of Timeout Parameter not supported") zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="847a1-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="847a1-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="847a1-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="847a1-131">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="847a1-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-132">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="847a1-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-133">**Unbekannter oder nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="847a1-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-134">**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="847a1-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-135">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="847a1-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-136">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="847a1-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-137">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="847a1-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-138">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="847a1-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-139">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="847a1-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-140">**Ungültiger Status Übergang** (4097).</span><span class="sxs-lookup"><span data-stu-id="847a1-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-141">**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)</span><span class="sxs-lookup"><span data-stu-id="847a1-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-142">**Ausgelastet** (4099)</span><span class="sxs-lookup"><span data-stu-id="847a1-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-143">**Reservierte Methode** (4100.32767)</span><span class="sxs-lookup"><span data-stu-id="847a1-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="847a1-144">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="847a1-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="847a1-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="847a1-145">Requirements</span></span>



| <span data-ttu-id="847a1-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="847a1-146">Requirement</span></span> | <span data-ttu-id="847a1-147">Wert</span><span class="sxs-lookup"><span data-stu-id="847a1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847a1-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="847a1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="847a1-149">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="847a1-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="847a1-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="847a1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="847a1-151">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="847a1-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="847a1-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="847a1-152">Namespace</span></span><br/>                | <span data-ttu-id="847a1-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="847a1-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="847a1-154">MOF</span><span class="sxs-lookup"><span data-stu-id="847a1-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="847a1-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="847a1-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="847a1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="847a1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="847a1-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="847a1-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="847a1-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="847a1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847a1-159">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="847a1-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




