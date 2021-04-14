---
title: Ivmvirtualmachineevents onhardplefault-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Onseriplefault-Methode virtueller PC
- Onseriplefault-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onseriplefault-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518563"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="af495-106">Ivmvirtualmachineevents:: onhardplefault-Methode</span><span class="sxs-lookup"><span data-stu-id="af495-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="af495-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af495-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="af495-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="af495-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="af495-109">Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="af495-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="af495-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="af495-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="af495-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="af495-111">Parameters</span></span>

<span data-ttu-id="af495-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="af495-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af495-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af495-113">Return value</span></span>

<span data-ttu-id="af495-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="af495-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af495-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af495-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af495-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af495-116">Remarks</span></span>

<span data-ttu-id="af495-117">Diese Methode wird aufgerufen, wenn ein virtueller Computer einen dreifachen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="af495-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="af495-118">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmvirtualmachineevent-Ereignis vom Typ "vmvirtualmachineevent" zu erhalten, das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)</span><span class="sxs-lookup"><span data-stu-id="af495-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af495-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af495-119">Requirements</span></span>



| <span data-ttu-id="af495-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af495-120">Requirement</span></span> | <span data-ttu-id="af495-121">Wert</span><span class="sxs-lookup"><span data-stu-id="af495-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="af495-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af495-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af495-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af495-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af495-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af495-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af495-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="af495-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="af495-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="af495-126">End of client support</span></span><br/>    | <span data-ttu-id="af495-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af495-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="af495-128">Produkt</span><span class="sxs-lookup"><span data-stu-id="af495-128">Product</span></span><br/>                  | <span data-ttu-id="af495-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="af495-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="af495-130">Header</span><span class="sxs-lookup"><span data-stu-id="af495-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="af495-131"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="af495-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="af495-132">IID</span><span class="sxs-lookup"><span data-stu-id="af495-132">IID</span></span><br/>                      | <span data-ttu-id="af495-133">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="af495-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="af495-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af495-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af495-135">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="af495-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

