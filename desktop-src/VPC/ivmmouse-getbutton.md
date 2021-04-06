---
title: Ivmmouse getbutton-Methode (vpccominterfaces. h)
description: Ruft den aktuellen Zustand der angegebenen Maustaste ab.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Getbutton-Methode virtueller PC
- Getbutton-Methode Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, getbutton-Methode
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743457"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="0ac4e-106">Ivmmouse:: getbutton-Methode</span><span class="sxs-lookup"><span data-stu-id="0ac4e-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="0ac4e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0ac4e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0ac4e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0ac4e-109">Ruft den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste ab.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac4e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ac4e-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="0ac4e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ac4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac4e-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ac4e-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac4e-113">Der Index der Schaltfläche, deren Zustand angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="0ac4e-114">Eine Liste der Werte finden Sie unter [**vmmousetbutton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="0ac4e-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ac4e-115">*isdown* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0ac4e-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac4e-116">Der Zustand der aufgeführten Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-116">The state of the indicated button.</span></span> <span data-ttu-id="0ac4e-117">**True** , wenn die Schaltfläche auf dem virtuellen Computer zurzeit nicht angezeigt wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0ac4e-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac4e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ac4e-118">Return value</span></span>

<span data-ttu-id="0ac4e-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-119">This method can return one of these values.</span></span>



| <span data-ttu-id="0ac4e-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0ac4e-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="0ac4e-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ac4e-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ac4e-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="0ac4e-123">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0ac4e-124"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="0ac4e-125">Der *isdown* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0ac4e-126"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="0ac4e-127">Der *Button Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0ac4e-128"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="0ac4e-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="0ac4e-129">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="0ac4e-130"><dt>**VM \_ E \_ Maus \_ nicht \_ aktiv**</dt> <dt>0xa0040800</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="0ac4e-131">Das Mausgerät wurde nicht eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0ac4e-132"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="0ac4e-133">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0ac4e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ac4e-134">Requirements</span></span>



| <span data-ttu-id="0ac4e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ac4e-135">Requirement</span></span> | <span data-ttu-id="0ac4e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0ac4e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac4e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ac4e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac4e-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ac4e-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ac4e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ac4e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac4e-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0ac4e-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0ac4e-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0ac4e-141">End of client support</span></span><br/>    | <span data-ttu-id="0ac4e-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ac4e-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0ac4e-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="0ac4e-143">Product</span></span><br/>                  | <span data-ttu-id="0ac4e-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0ac4e-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0ac4e-145">Header</span><span class="sxs-lookup"><span data-stu-id="0ac4e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac4e-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4e-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0ac4e-147">IID</span><span class="sxs-lookup"><span data-stu-id="0ac4e-147">IID</span></span><br/>                      | <span data-ttu-id="0ac4e-148">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="0ac4e-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="0ac4e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ac4e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac4e-150">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="0ac4e-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

