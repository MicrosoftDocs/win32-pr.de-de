---
title: Ivmvirtualmachineevents ondiskouesfspace-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass der freie Speicherplatz auf einem für einen virtuellen Computer erforderlichen Datenträger gering ist.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Ondiskoudef Space-Methode virtueller PC
- Ondiskoudef Space-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, ondiskouesf Space-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858625"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="36442-106">Ivmvirtualmachineevents:: ondiskoudef Space-Methode</span><span class="sxs-lookup"><span data-stu-id="36442-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="36442-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36442-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="36442-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="36442-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="36442-109">Empfängt eine Benachrichtigung, dass der freie Speicherplatz für einen virtuellen Computer (VM) nicht ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="36442-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="36442-110">Fällt der freie Speicherplatz unter 100 MB, wird dieses Ereignis als Warnung empfangen, und wenn der freie Speicherplatz unter 20 MB sinkt, wird dieses Ereignis erneut als Fehler empfangen, und der virtuelle Computer wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="36442-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="36442-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="36442-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="36442-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36442-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36442-113">*criticallylow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36442-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36442-114">Legen Sie diese Einstellung auf **Variant \_ true** fest, wenn der Datenträger weniger als 20 MB frei ist, und auf **\_ false** , wenn der freie Speicherplatz größer als 20 MB, aber kleiner als 100 MB ist.</span><span class="sxs-lookup"><span data-stu-id="36442-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36442-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36442-115">Return value</span></span>

<span data-ttu-id="36442-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="36442-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36442-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36442-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="36442-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36442-118">Requirements</span></span>



| <span data-ttu-id="36442-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36442-119">Requirement</span></span> | <span data-ttu-id="36442-120">Wert</span><span class="sxs-lookup"><span data-stu-id="36442-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36442-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36442-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36442-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36442-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36442-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36442-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36442-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="36442-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="36442-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="36442-125">End of client support</span></span><br/>    | <span data-ttu-id="36442-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36442-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="36442-127">Produkt</span><span class="sxs-lookup"><span data-stu-id="36442-127">Product</span></span><br/>                  | <span data-ttu-id="36442-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="36442-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="36442-129">Header</span><span class="sxs-lookup"><span data-stu-id="36442-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="36442-130"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="36442-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="36442-131">IID</span><span class="sxs-lookup"><span data-stu-id="36442-131">IID</span></span><br/>                      | <span data-ttu-id="36442-132">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="36442-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="36442-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36442-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36442-134">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="36442-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

