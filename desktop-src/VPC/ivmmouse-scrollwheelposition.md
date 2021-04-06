---
title: Ivmmouse scrollwheelposition-Eigenschaft (vpccominterfaces. h)
description: Passt die z-Koordinate der Maus an (nur relativ).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Scrollwheelposition-Eigenschaft virtueller PC
- Scrollwheelposition-Eigenschaft Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, scrollwheelposition (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743456"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="d974d-106">Ivmmouse:: scrollwheelposition (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d974d-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="d974d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d974d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d974d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d974d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d974d-109">Passt die z-Koordinate der Maus an (nur relativ).</span><span class="sxs-lookup"><span data-stu-id="d974d-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="d974d-110">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="d974d-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d974d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d974d-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="d974d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d974d-112">Property value</span></span>

<span data-ttu-id="d974d-113">Die z-Koordinate, die die Anzahl der Pixel angibt, die die Maus entlang der z-Achse verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d974d-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d974d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d974d-114">Error codes</span></span>



| <span data-ttu-id="d974d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d974d-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="d974d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d974d-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d974d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d974d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="d974d-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d974d-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="d974d-119"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="d974d-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="d974d-120">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d974d-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="d974d-121"><dt>VM \_ E \_ Maus \_ nicht \_ aktiv</dt> <dt>0xa0040800</dt></span><span class="sxs-lookup"><span data-stu-id="d974d-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="d974d-122">Das Mausgerät wurde nicht eingeschaltet oder ist auf dem virtuellen Computer zurzeit nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="d974d-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="d974d-123"><dt>VM \_ E \_ verwenden \_ absoluter \_ Koordinaten</dt> <dt>0xa0040801</dt></span><span class="sxs-lookup"><span data-stu-id="d974d-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="d974d-124">Die scrollradposition kann nicht festgelegt werden, wenn das Mausgerät absolute Koordinaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="d974d-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="d974d-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d974d-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="d974d-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d974d-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="d974d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d974d-127">Requirements</span></span>



| <span data-ttu-id="d974d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d974d-128">Requirement</span></span> | <span data-ttu-id="d974d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d974d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d974d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d974d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d974d-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d974d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d974d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d974d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d974d-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d974d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d974d-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d974d-134">End of client support</span></span><br/>    | <span data-ttu-id="d974d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d974d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d974d-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="d974d-136">Product</span></span><br/>                  | <span data-ttu-id="d974d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d974d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d974d-138">Header</span><span class="sxs-lookup"><span data-stu-id="d974d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d974d-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d974d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d974d-140">IID</span><span class="sxs-lookup"><span data-stu-id="d974d-140">IID</span></span><br/>                      | <span data-ttu-id="d974d-141">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="d974d-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="d974d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d974d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d974d-143">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="d974d-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

