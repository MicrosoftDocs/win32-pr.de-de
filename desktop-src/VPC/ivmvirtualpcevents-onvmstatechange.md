---
title: Ivmvirtualpcevents onvmstatechange-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat. | Ivmvirtualpcevents onvmstatechange-Methode (vpccominterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Onvmstatechange-Methode Virtual PC
- Onvmstatechange-Methode Virtual PC, ivmvirtualpcevents-Schnittstelle
- Ivmvirtualpcevents Interface Virtual PC, onvmstatechange-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363927"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="9ef96-107">Ivmvirtualpcevents:: onvmstatechange-Methode</span><span class="sxs-lookup"><span data-stu-id="9ef96-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="9ef96-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ef96-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9ef96-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9ef96-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9ef96-110">Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9ef96-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef96-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef96-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="9ef96-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef96-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef96-113">*virtualmachineconfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ef96-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef96-114">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9ef96-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="9ef96-115">*virtualmachinestate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ef96-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef96-116">Der neue Zustand der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="9ef96-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef96-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ef96-117">Return value</span></span>

<span data-ttu-id="9ef96-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9ef96-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ef96-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ef96-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef96-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ef96-120">Remarks</span></span>

<span data-ttu-id="9ef96-121">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das **\_ vmstatechanged** -Ereignis von [**ivmvirtualpc**](ivmvirtualpc.md)empfangen zu können.</span><span class="sxs-lookup"><span data-stu-id="9ef96-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="9ef96-122">Um einen bestimmten virtuellen Computer zu überwachen, verwenden Sie die [**ivmvirtualmachineevents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9ef96-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef96-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ef96-123">Requirements</span></span>



| <span data-ttu-id="9ef96-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ef96-124">Requirement</span></span> | <span data-ttu-id="9ef96-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9ef96-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef96-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ef96-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef96-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ef96-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ef96-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ef96-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef96-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ef96-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9ef96-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9ef96-130">End of client support</span></span><br/>    | <span data-ttu-id="9ef96-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ef96-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9ef96-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="9ef96-132">Product</span></span><br/>                  | <span data-ttu-id="9ef96-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9ef96-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9ef96-134">Header</span><span class="sxs-lookup"><span data-stu-id="9ef96-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef96-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef96-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9ef96-136">IID</span><span class="sxs-lookup"><span data-stu-id="9ef96-136">IID</span></span><br/>                      | <span data-ttu-id="9ef96-137">Diid \_ ivmvirtualpcevents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.</span><span class="sxs-lookup"><span data-stu-id="9ef96-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9ef96-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ef96-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef96-139">**Ivmvirtualpcevents**</span><span class="sxs-lookup"><span data-stu-id="9ef96-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

