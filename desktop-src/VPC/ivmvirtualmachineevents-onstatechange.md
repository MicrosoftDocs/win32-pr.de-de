---
title: Ivmvirtualmachineevents OnStateChange-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat. | Ivmvirtualmachineevents OnStateChange-Methode (vpccominterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- OnStateChange-Methode Virtual PC
- OnStateChange-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, OnStateChange-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353819"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="88fa5-107">Ivmvirtualmachineevents:: OnStateChange-Methode</span><span class="sxs-lookup"><span data-stu-id="88fa5-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="88fa5-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88fa5-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88fa5-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88fa5-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88fa5-110">Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.</span><span class="sxs-lookup"><span data-stu-id="88fa5-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="88fa5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="88fa5-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="88fa5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="88fa5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88fa5-113">*virtualmachinestate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88fa5-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88fa5-114">Der neue Zustand der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="88fa5-114">The new state of the virtual machine.</span></span> <span data-ttu-id="88fa5-115">Eine Liste der Werte finden Sie unter [**vmvmstate**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="88fa5-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88fa5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88fa5-116">Return value</span></span>

<span data-ttu-id="88fa5-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="88fa5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88fa5-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88fa5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88fa5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88fa5-119">Remarks</span></span>

<span data-ttu-id="88fa5-120">Diese Methode wird aufgerufen, wenn sich der Zustand für diesen virtuellen Computer ändert.</span><span class="sxs-lookup"><span data-stu-id="88fa5-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="88fa5-121">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammende StateChanged-Ereignis vmvirtualmachineevent zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="88fa5-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88fa5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88fa5-122">Requirements</span></span>



| <span data-ttu-id="88fa5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88fa5-123">Requirement</span></span> | <span data-ttu-id="88fa5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="88fa5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fa5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88fa5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="88fa5-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88fa5-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88fa5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88fa5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="88fa5-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88fa5-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88fa5-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="88fa5-129">End of client support</span></span><br/>    | <span data-ttu-id="88fa5-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88fa5-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88fa5-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="88fa5-131">Product</span></span><br/>                  | <span data-ttu-id="88fa5-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88fa5-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88fa5-133">Header</span><span class="sxs-lookup"><span data-stu-id="88fa5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="88fa5-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fa5-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88fa5-135">IID</span><span class="sxs-lookup"><span data-stu-id="88fa5-135">IID</span></span><br/>                      | <span data-ttu-id="88fa5-136">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="88fa5-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="88fa5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88fa5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fa5-138">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="88fa5-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

