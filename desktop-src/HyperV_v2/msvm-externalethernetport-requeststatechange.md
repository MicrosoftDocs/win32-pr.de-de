---
description: 'RequestStateChange-Methode der Msvm_ExternalEthernetPort-Klasse: Fordert eine Zustandsänderung an.'
ms.assetid: 57d863bd-7fa2-4291-99bf-42ac4f813d59
title: RequestStateChange-Methode der Msvm_ExternalEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9a9f135e65527b252fbe1c3da0345655b5c14c72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111897"
---
# <a name="requeststatechange-method-of-the-msvm_externalethernetport-class"></a><span data-ttu-id="8e4a6-103">RequestStateChange-Methode der Msvm \_ ExternalEthernetPort-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e4a6-103">RequestStateChange method of the Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="8e4a6-104">Fordert eine Zustandsänderung an.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4a6-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="8e4a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e4a6-107">*RequestedState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8e4a6-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4a6-108">Der neue Zustand.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-108">The new state.</span></span> <span data-ttu-id="8e4a6-109">Die Informationen werden in die **RequestedState-Eigenschaft** der -Instanz platziert, wenn der Rückgabecode der **RequestStateChange-Methode** 0 oder 4096 ist.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="8e4a6-110">Weitere Informationen finden Sie in der Beschreibung der **Eigenschaften EnabledState** und **RequestedState** für das -Element.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="8e4a6-111">Dies muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8e4a6-112">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e4a6-113">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8e4a6-114">**Herunterfahren** (4)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8e4a6-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8e4a6-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8e4a6-117">**Zurückstellen** (8)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8e4a6-118">**Stille** (9)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8e4a6-119">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8e4a6-120">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8e4a6-121">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8e4a6-122">**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8e4a6-123">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e4a6-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4a6-124">Kann einen Verweis auf den [**CIM \_ ConcreteJob**](cim-concretejob.md) enthalten, der erstellt wurde, um den zustandsübergang zu verfolgen, der durch den Methodenaufruf initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="8e4a6-125">*TimeoutPeriod* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8e4a6-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e4a6-126">Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="8e4a6-127">Das Intervallformat muss verwendet werden, um den Timeoutzeitraum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="8e4a6-128">Der Wert 0 oder **NULL gibt an,** dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="8e4a6-129">Wenn diese Eigenschaft nicht 0 oder **NULL** enthält und die Implementierung diesen Parameter nicht unterstützt, muss der Rückgabecode 4098 (**Use Of Timeout Parameter Not Supported**) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e4a6-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e4a6-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e4a6-130">Return value</span></span>

<span data-ttu-id="8e4a6-131">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="8e4a6-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8e4a6-132">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e4a6-133">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8e4a6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e4a6-134">Requirements</span></span>



| <span data-ttu-id="8e4a6-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e4a6-135">Requirement</span></span> | <span data-ttu-id="8e4a6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8e4a6-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4a6-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4a6-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8e4a6-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8e4a6-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e4a6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4a6-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8e4a6-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8e4a6-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e4a6-141">Namespace</span></span><br/>                | <span data-ttu-id="8e4a6-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e4a6-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e4a6-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8e4a6-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e4a6-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e4a6-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e4a6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8e4a6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e4a6-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e4a6-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e4a6-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e4a6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4a6-148">**Msvm \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="8e4a6-148">**Msvm\_ExternalEthernetPort**</span></span>](msvm-externalethernetport.md)
</dt> </dl>

 

 




