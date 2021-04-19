---
description: Fordert eine Statusänderung an.
ms.assetid: ae799e76-5177-42a5-8591-ceaf15dd7eaf
title: RequestStateChange-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8a09d520d9b902663e39999aae3e949723d2e128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350256"
---
# <a name="requeststatechange-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d2ad3-103">RequestStateChange-Methode der MSVM \_ replicationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d2ad3-103">RequestStateChange method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d2ad3-104">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ad3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ad3-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="d2ad3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ad3-107">*Requestedstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ad3-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ad3-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-108">The new state.</span></span> <span data-ttu-id="d2ad3-109">Die Informationen werden in der **requestedstate** -Eigenschaft der-Instanz abgelegt, wenn der Rückgabecode der **requestStateChange** -Methode 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="d2ad3-110">Weitere Informationen finden Sie in der Beschreibung der Eigenschaften **enabledstate** und **requestedstate** für das-Element.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="d2ad3-111">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="d2ad3-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d2ad3-112">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d2ad3-113">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="d2ad3-114">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="d2ad3-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="d2ad3-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="d2ad3-117">Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="d2ad3-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="d2ad3-118">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="d2ad3-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="d2ad3-119">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="d2ad3-120">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d2ad3-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d2ad3-122">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d2ad3-123">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2ad3-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ad3-124">Kann einen Verweis auf den erstellten [**CIM- \_ bettejob**](cim-concretejob.md) enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="d2ad3-125">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ad3-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ad3-126">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="d2ad3-127">Das Intervall Format muss zum Angeben des Timeout Zeitraums verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="d2ad3-128">Der Wert 0 oder **null** zeigt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="d2ad3-129">Wenn diese Eigenschaft nicht 0 oder **null** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**use of Timeout Parameter not supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d2ad3-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ad3-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2ad3-130">Return value</span></span>

<span data-ttu-id="d2ad3-131">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="d2ad3-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d2ad3-132">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ad3-133">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2ad3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2ad3-134">Requirements</span></span>



| <span data-ttu-id="d2ad3-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2ad3-135">Requirement</span></span> | <span data-ttu-id="d2ad3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d2ad3-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ad3-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ad3-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d2ad3-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d2ad3-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2ad3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ad3-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d2ad3-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d2ad3-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2ad3-141">Namespace</span></span><br/>                | <span data-ttu-id="d2ad3-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2ad3-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d2ad3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ad3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ad3-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d2ad3-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ad3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ad3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ad3-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2ad3-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2ad3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2ad3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ad3-148">**MSVM \_ replicationservice**</span><span class="sxs-lookup"><span data-stu-id="d2ad3-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




