---
title: Ivmvirtualmachineevents onheartbeatbeendete-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Onheartbeatbeendete-Methode Virtual PC
- Onheartbeatbeendete-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onheartbeatbeendete-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956951"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="db222-106">Ivmvirtualmachineevents:: onheartbeatbeendete-Methode</span><span class="sxs-lookup"><span data-stu-id="db222-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="db222-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db222-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="db222-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="db222-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="db222-109">Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="db222-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="db222-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="db222-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="db222-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="db222-111">Parameters</span></span>

<span data-ttu-id="db222-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="db222-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db222-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db222-113">Return value</span></span>

<span data-ttu-id="db222-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="db222-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db222-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db222-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="db222-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db222-116">Remarks</span></span>

<span data-ttu-id="db222-117">Diese Methode wird aufgerufen, wenn das Gast Betriebssystem für diesen virtuellen Computer abrupt beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="db222-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="db222-118">Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das \_ vom [**ivmvirtualmachine**](ivmvirtualmachine.md)-Ereignis empfangene vmvirtualmachineevent heartbeatbeendeten-Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="db222-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db222-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db222-119">Requirements</span></span>



| <span data-ttu-id="db222-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db222-120">Requirement</span></span> | <span data-ttu-id="db222-121">Wert</span><span class="sxs-lookup"><span data-stu-id="db222-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db222-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db222-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db222-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db222-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db222-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db222-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db222-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db222-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="db222-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="db222-126">End of client support</span></span><br/>    | <span data-ttu-id="db222-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db222-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="db222-128">Produkt</span><span class="sxs-lookup"><span data-stu-id="db222-128">Product</span></span><br/>                  | <span data-ttu-id="db222-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="db222-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="db222-130">Header</span><span class="sxs-lookup"><span data-stu-id="db222-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="db222-131"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="db222-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="db222-132">IID</span><span class="sxs-lookup"><span data-stu-id="db222-132">IID</span></span><br/>                      | <span data-ttu-id="db222-133">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="db222-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="db222-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db222-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db222-135">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="db222-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

