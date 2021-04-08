---
title: Ivmvirtualmachineevents onreset-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Onreset-Methode Virtual PC
- Onreset-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onreset-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949377"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="90433-106">Ivmvirtualmachineevents:: onreset-Methode</span><span class="sxs-lookup"><span data-stu-id="90433-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="90433-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90433-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="90433-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="90433-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="90433-109">Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="90433-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="90433-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="90433-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="90433-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="90433-111">Parameters</span></span>

<span data-ttu-id="90433-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="90433-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90433-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90433-113">Return value</span></span>

<span data-ttu-id="90433-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="90433-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90433-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90433-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90433-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90433-116">Remarks</span></span>

<span data-ttu-id="90433-117">Diese Methode wird aufgerufen, wenn der virtuelle Computer zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="90433-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="90433-118">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmvirtualmachineevent Reset-Ereignis zu erhalten, das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="90433-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90433-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90433-119">Requirements</span></span>



| <span data-ttu-id="90433-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90433-120">Requirement</span></span> | <span data-ttu-id="90433-121">Wert</span><span class="sxs-lookup"><span data-stu-id="90433-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="90433-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90433-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90433-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90433-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90433-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90433-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90433-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90433-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="90433-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="90433-126">End of client support</span></span><br/>    | <span data-ttu-id="90433-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90433-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="90433-128">Produkt</span><span class="sxs-lookup"><span data-stu-id="90433-128">Product</span></span><br/>                  | <span data-ttu-id="90433-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="90433-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="90433-130">Header</span><span class="sxs-lookup"><span data-stu-id="90433-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="90433-131"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="90433-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="90433-132">IID</span><span class="sxs-lookup"><span data-stu-id="90433-132">IID</span></span><br/>                      | <span data-ttu-id="90433-133">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="90433-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="90433-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90433-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90433-135">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="90433-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

