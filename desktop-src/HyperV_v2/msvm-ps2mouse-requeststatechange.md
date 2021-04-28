---
description: RequestStateChange-Methode der Msvm_Ps2Mouse - Fordert eine Zustandsänderung an.
ms.assetid: a61c17a8-f89d-47aa-8c4f-46ccf478103e
title: RequestStateChange-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 878b0977a244d4b098dfa449f3c778c33e909111
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118818"
---
# <a name="requeststatechange-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="8b3dd-103">RequestStateChange-Methode der Msvm \_ Ps2Mouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b3dd-103">RequestStateChange method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="8b3dd-104">Fordert eine Zustandsänderung an.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b3dd-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="8b3dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b3dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3dd-107">*RequestedState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8b3dd-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3dd-108">Der für das Element angeforderte Zustand.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-108">The state requested for the element.</span></span> <span data-ttu-id="8b3dd-109">Diese Informationen werden in die RequestedState-Eigenschaft der -Instanz platziert, wenn der Rückgabecode der RequestStateChange-Methode 0 ('Completed with No Error') oder 4096 (0x1000) ('Job Started') ist.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="8b3dd-110">Ausführliche Erläuterungen zu den RequestedState-Werten finden Sie in der Beschreibung der Eigenschaften EnabledState und RequestedState.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8b3dd-111">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8b3dd-112">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8b3dd-113">**Herunterfahren** (4)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8b3dd-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8b3dd-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8b3dd-116">**Zurückern** (8)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8b3dd-117">**Ruhe** (9)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8b3dd-118">**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8b3dd-119">**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8b3dd-120">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8b3dd-121">**Reservierter Anbieter** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8b3dd-122">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b3dd-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3dd-123">Kann einen Verweis auf den ConcreteJob enthalten, der erstellt wurde, um den Zustandsübergang nachzuverfolgen, der durch den Methodenaufruf initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="8b3dd-124">*TimeoutPeriod* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8b3dd-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3dd-125">Ein Timeoutzeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="8b3dd-126">Das Intervallformat muss verwendet werden, um timeoutPeriod anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="8b3dd-127">Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="8b3dd-128">Wenn diese Eigenschaft nicht 0 oder NULL enthält und die Implementierung diesen Parameter nicht unterstützt, wird der Rückgabecode "Use Of Timeout Parameter Not Supported" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b3dd-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b3dd-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b3dd-129">Return value</span></span>

<span data-ttu-id="8b3dd-130">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="8b3dd-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8b3dd-131">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b3dd-132">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8b3dd-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b3dd-133">Requirements</span></span>



| <span data-ttu-id="8b3dd-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b3dd-134">Requirement</span></span> | <span data-ttu-id="8b3dd-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8b3dd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3dd-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8b3dd-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8b3dd-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8b3dd-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b3dd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8b3dd-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8b3dd-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8b3dd-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b3dd-140">Namespace</span></span><br/>                | <span data-ttu-id="8b3dd-141">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b3dd-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b3dd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8b3dd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b3dd-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b3dd-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b3dd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8b3dd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b3dd-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b3dd-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b3dd-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b3dd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3dd-147">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="8b3dd-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

 




