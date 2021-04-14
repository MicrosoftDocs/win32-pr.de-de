---
title: Ivmmouse-Click-Methode (vpccominterfaces. h)
description: Simuliert das Klicken auf die Maustaste.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Klicken Sie auf method Virtual PC.
- Klicken Sie auf Methode Virtual PC, ivmmouse Interface.
- Ivmmouse Interface Virtual PC, klicken Sie auf Methode.
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478999"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="a51a8-106">Ivmmouse:: Click-Methode</span><span class="sxs-lookup"><span data-stu-id="a51a8-106">IVMMouse::Click method</span></span>

<span data-ttu-id="a51a8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a51a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a51a8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a51a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a51a8-109">Simuliert das Klicken auf die Maustaste.</span><span class="sxs-lookup"><span data-stu-id="a51a8-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51a8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a51a8-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="a51a8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a51a8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a51a8-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a51a8-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a51a8-113">Der Index der Schaltfläche, auf die geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="a51a8-113">The index of the button being clicked.</span></span> <span data-ttu-id="a51a8-114">Eine Liste der Werte finden Sie unter [**vmmousetbutton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="a51a8-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a51a8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a51a8-115">Return value</span></span>

<span data-ttu-id="a51a8-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a51a8-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a51a8-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a51a8-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="a51a8-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a51a8-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a51a8-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="a51a8-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a51a8-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="a51a8-121"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="a51a8-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a51a8-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="a51a8-123"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="a51a8-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="a51a8-124">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a51a8-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="a51a8-125"><dt>**VM \_ E \_ Maus \_ nicht \_ aktiv**</dt> <dt>0xa0040800</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="a51a8-126">Der Vorgang konnte nicht abgeschlossen werden, da das Mausgerät nicht eingeschaltet ist oder derzeit nicht auf dem virtuellen Computer aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a51a8-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="a51a8-127"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="a51a8-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a51a8-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="a51a8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a51a8-129">Requirements</span></span>



| <span data-ttu-id="a51a8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a51a8-130">Requirement</span></span> | <span data-ttu-id="a51a8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a51a8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51a8-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a51a8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a51a8-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a51a8-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a51a8-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a51a8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a51a8-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a51a8-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a51a8-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a51a8-136">End of client support</span></span><br/>    | <span data-ttu-id="a51a8-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a51a8-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a51a8-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="a51a8-138">Product</span></span><br/>                  | <span data-ttu-id="a51a8-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a51a8-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a51a8-140">Header</span><span class="sxs-lookup"><span data-stu-id="a51a8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a51a8-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51a8-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a51a8-142">IID</span><span class="sxs-lookup"><span data-stu-id="a51a8-142">IID</span></span><br/>                      | <span data-ttu-id="a51a8-143">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="a51a8-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="a51a8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a51a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51a8-145">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="a51a8-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

