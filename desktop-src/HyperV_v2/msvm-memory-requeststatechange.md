---
description: Fordert eine Statusänderung an.
ms.assetid: 836ee3a1-e28e-4f84-8e1c-09f4a2ff0a25
title: RequestStateChange-Methode der Msvm_Memory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 761a486f21f6c1cd8c61978038cc2d37bba8c288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349058"
---
# <a name="requeststatechange-method-of-the-msvm_memory-class"></a><span data-ttu-id="1daa3-103">RequestStateChange-Methode der MSVM- \_ Speicher Klasse</span><span class="sxs-lookup"><span data-stu-id="1daa3-103">RequestStateChange method of the Msvm\_Memory class</span></span>

<span data-ttu-id="1daa3-104">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="1daa3-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="1daa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1daa3-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="1daa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1daa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1daa3-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1daa3-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daa3-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="1daa3-108">The new state.</span></span> <span data-ttu-id="1daa3-109">Die Informationen werden in der **requestedstate** -Eigenschaft der-Instanz abgelegt, wenn der Rückgabecode der **requestStateChange** -Methode 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="1daa3-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="1daa3-110">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** für das-Element.</span><span class="sxs-lookup"><span data-stu-id="1daa3-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="1daa3-111">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="1daa3-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1daa3-112">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="1daa3-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1daa3-113">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="1daa3-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="1daa3-114">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="1daa3-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="1daa3-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="1daa3-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="1daa3-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="1daa3-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="1daa3-117">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="1daa3-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="1daa3-118">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="1daa3-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="1daa3-119">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="1daa3-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="1daa3-120">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="1daa3-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1daa3-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1daa3-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1daa3-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="1daa3-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1daa3-123">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1daa3-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1daa3-124">Kann einen Verweis auf den erstellten [**CIM- \_ bettejob**](cim-concretejob.md) enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="1daa3-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="1daa3-125">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1daa3-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1daa3-126">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="1daa3-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="1daa3-127">Zum Angeben des timeoutperiod muss das Intervall Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1daa3-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="1daa3-128">Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="1daa3-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="1daa3-129">Wenn diese Eigenschaft nicht 0 oder NULL enthält und die Implementierung diesen Parameter nicht unterstützt, sollte der Rückgabecode "Use of Timeout Parameter not supported" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1daa3-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1daa3-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1daa3-130">Return value</span></span>

<span data-ttu-id="1daa3-131">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="1daa3-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1daa3-132">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="1daa3-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1daa3-133">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1daa3-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1daa3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1daa3-134">Requirements</span></span>



| <span data-ttu-id="1daa3-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1daa3-135">Requirement</span></span> | <span data-ttu-id="1daa3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1daa3-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1daa3-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1daa3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1daa3-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1daa3-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1daa3-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1daa3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1daa3-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1daa3-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1daa3-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1daa3-141">Namespace</span></span><br/>                | <span data-ttu-id="1daa3-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1daa3-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1daa3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1daa3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1daa3-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1daa3-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1daa3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1daa3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1daa3-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1daa3-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1daa3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1daa3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1daa3-148">**MSVM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="1daa3-148">**Msvm\_Memory**</span></span>](msvm-memory.md)
</dt> </dl>

 

 




