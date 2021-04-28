---
description: 'RequestStateChange-Methode der Msvm_VssComponent-Klasse: Fordert eine Zustandsänderung an.'
ms.assetid: 27a8ab6e-afbd-4d87-afd6-8da0cc5e3fba
title: RequestStateChange-Methode der Msvm_VssComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f75d0e2eed242155f27a7355182bf616d14de7e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109268"
---
# <a name="requeststatechange-method-of-the-msvm_vsscomponent-class"></a><span data-ttu-id="656b4-103">RequestStateChange-Methode der Msvm \_ VssComponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="656b4-103">RequestStateChange method of the Msvm\_VssComponent class</span></span>

<span data-ttu-id="656b4-104">Fordert eine Zustandsänderung an.</span><span class="sxs-lookup"><span data-stu-id="656b4-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="656b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="656b4-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="656b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="656b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656b4-107">*RequestedState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="656b4-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656b4-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="656b4-108">The new state.</span></span> <span data-ttu-id="656b4-109">Die Informationen werden in die **RequestedState-Eigenschaft** der -Instanz platziert, wenn der Rückgabecode der **RequestStateChange-Methode** 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="656b4-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="656b4-110">Weitere Informationen finden Sie in der Beschreibung der **Eigenschaften EnabledState** und **RequestedState** für das -Element.</span><span class="sxs-lookup"><span data-stu-id="656b4-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="656b4-111">Dies muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="656b4-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="656b4-112">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="656b4-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="656b4-113">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="656b4-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="656b4-114">**Herunterfahren** (4)</span><span class="sxs-lookup"><span data-stu-id="656b4-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="656b4-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="656b4-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="656b4-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="656b4-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="656b4-117">**Zurückstellen** (8)</span><span class="sxs-lookup"><span data-stu-id="656b4-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="656b4-118">**Stille** (9)</span><span class="sxs-lookup"><span data-stu-id="656b4-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="656b4-119">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="656b4-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="656b4-120">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="656b4-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="656b4-121">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="656b4-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="656b4-122">**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="656b4-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="656b4-123">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="656b4-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="656b4-124">Kann einen Verweis auf den [**CIM \_ ConcreteJob**](cim-concretejob.md) enthalten, der erstellt wurde, um den durch den Methodenaufruf initiierten Zustandsübergang nachverfolgung zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="656b4-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="656b4-125">*TimeoutPeriod* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="656b4-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656b4-126">Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="656b4-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="656b4-127">Das Intervallformat muss verwendet werden, um **timeoutPeriod anzugeben.**</span><span class="sxs-lookup"><span data-stu-id="656b4-127">The interval format must be used to specify the **TimeoutPeriod**.</span></span> <span data-ttu-id="656b4-128">Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="656b4-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="656b4-129">Wenn diese Eigenschaft nicht 0 oder NULL enthält und die Implementierung diesen Parameter nicht unterstützt, wird der Rückgabecode "Use Of Timeout Parameter Not Supported" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="656b4-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656b4-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="656b4-130">Return value</span></span>

<span data-ttu-id="656b4-131">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="656b4-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="656b4-132">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="656b4-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="656b4-133">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="656b4-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="656b4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656b4-134">Requirements</span></span>



| <span data-ttu-id="656b4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656b4-135">Requirement</span></span> | <span data-ttu-id="656b4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="656b4-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656b4-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="656b4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="656b4-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="656b4-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="656b4-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="656b4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="656b4-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="656b4-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="656b4-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="656b4-141">Namespace</span></span><br/>                | <span data-ttu-id="656b4-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="656b4-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="656b4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="656b4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="656b4-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="656b4-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="656b4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="656b4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="656b4-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="656b4-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="656b4-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="656b4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656b4-148">**Msvm \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="656b4-148">**Msvm\_VssComponent**</span></span>](msvm-vsscomponent.md)
</dt> </dl>

 

 




