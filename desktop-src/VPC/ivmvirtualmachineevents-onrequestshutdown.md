---
title: Ivmvirtualmachineevents onrequestshutdown-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Onrequestshutdown-Methode virtueller PC
- Onrequestshutdown-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onrequestshutdown-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477403"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="d92ed-106">Ivmvirtualmachineevents:: onrequestshutdown-Methode</span><span class="sxs-lookup"><span data-stu-id="d92ed-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="d92ed-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d92ed-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d92ed-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d92ed-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d92ed-109">Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d92ed-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92ed-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d92ed-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="d92ed-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d92ed-111">Parameters</span></span>

<span data-ttu-id="d92ed-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d92ed-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d92ed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d92ed-113">Return value</span></span>

<span data-ttu-id="d92ed-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d92ed-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d92ed-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d92ed-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92ed-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d92ed-116">Remarks</span></span>

<span data-ttu-id="d92ed-117">Diese Methode wird immer dann aufgerufen, wenn die Sitzung des virtuellen Computers gerade heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d92ed-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="d92ed-118">Das Client Programm muss diese Schnittstellen Methode implementieren, um eine Benachrichtigung über das " **vmvirtualmachineevent \_ requestshutdown** "-Ereignis zu erhalten, das von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="d92ed-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="d92ed-119">Diese Ereignis Benachrichtigung wird nur gesendet, wenn die Sitzung der virtuellen Computer gerade heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d92ed-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="d92ed-120">Die Routinen zum Herunterfahren des Betriebssystems, wie z. b. [**ivmguestos:: Shutdown**](ivmguestos-shutdown.md), lösen dieses Ereignis nicht direkt aus, es sei denn, Sie versuchen auch, ein Software ausschalten der virtuellen Hardware auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d92ed-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d92ed-121">Requirements</span></span>



| <span data-ttu-id="d92ed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d92ed-122">Requirement</span></span> | <span data-ttu-id="d92ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d92ed-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92ed-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d92ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d92ed-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d92ed-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d92ed-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d92ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d92ed-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d92ed-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d92ed-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d92ed-128">End of client support</span></span><br/>    | <span data-ttu-id="d92ed-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d92ed-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d92ed-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="d92ed-130">Product</span></span><br/>                  | <span data-ttu-id="d92ed-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d92ed-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d92ed-132">Header</span><span class="sxs-lookup"><span data-stu-id="d92ed-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92ed-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92ed-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d92ed-134">IID</span><span class="sxs-lookup"><span data-stu-id="d92ed-134">IID</span></span><br/>                      | <span data-ttu-id="d92ed-135">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="d92ed-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d92ed-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d92ed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92ed-137">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="d92ed-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

