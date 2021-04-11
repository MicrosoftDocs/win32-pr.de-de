---
title: Ivmmouse setbutton-Methode (vpccominterfaces. h)
description: Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Setbutton-Methode virtueller PC
- Setbutton-Methode Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, setbutton-Methode
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105675"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="ee735-106">Ivmmouse:: setbutton-Methode</span><span class="sxs-lookup"><span data-stu-id="ee735-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="ee735-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee735-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ee735-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ee735-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ee735-109">Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.</span><span class="sxs-lookup"><span data-stu-id="ee735-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee735-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee735-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="ee735-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee735-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee735-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee735-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-113">Der Schaltflächen Index.</span><span class="sxs-lookup"><span data-stu-id="ee735-113">The button index.</span></span> <span data-ttu-id="ee735-114">Eine Liste der Werte finden Sie unter [**vmmousetbutton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="ee735-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee735-115">*nach unten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee735-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee735-116">Der neue Schaltflächen Zustand.</span><span class="sxs-lookup"><span data-stu-id="ee735-116">The new button state.</span></span> <span data-ttu-id="ee735-117">Verwenden Sie **true** , wenn der Zustand der Schaltfläche auf Down festgelegt werden soll, und **false** , wenn es auf up festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee735-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee735-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee735-118">Return value</span></span>

<span data-ttu-id="ee735-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ee735-119">This method can return one of these values.</span></span>



| <span data-ttu-id="ee735-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ee735-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="ee735-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee735-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee735-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="ee735-123">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee735-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="ee735-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="ee735-125">Der *Button Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ee735-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="ee735-126"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="ee735-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="ee735-127">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee735-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="ee735-128"><dt>**VM \_ E \_ Maus \_ nicht \_ aktiv**</dt> <dt>0xa0040800</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="ee735-129">Der Vorgang konnte nicht abgeschlossen werden, da das Mausgerät nicht eingeschaltet ist oder derzeit nicht auf dem virtuellen Computer aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ee735-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="ee735-130"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="ee735-131">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ee735-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="ee735-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee735-132">Requirements</span></span>



| <span data-ttu-id="ee735-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee735-133">Requirement</span></span> | <span data-ttu-id="ee735-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ee735-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee735-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee735-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ee735-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee735-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee735-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee735-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ee735-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ee735-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ee735-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ee735-139">End of client support</span></span><br/>    | <span data-ttu-id="ee735-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee735-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ee735-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="ee735-141">Product</span></span><br/>                  | <span data-ttu-id="ee735-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ee735-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ee735-143">Header</span><span class="sxs-lookup"><span data-stu-id="ee735-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee735-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee735-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ee735-145">IID</span><span class="sxs-lookup"><span data-stu-id="ee735-145">IID</span></span><br/>                      | <span data-ttu-id="ee735-146">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="ee735-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ee735-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee735-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee735-148">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="ee735-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

