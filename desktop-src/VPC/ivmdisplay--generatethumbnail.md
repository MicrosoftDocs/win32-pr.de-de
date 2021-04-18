---
title: Ivmdisplay-_GenerateThumbnail Methode (vpccominterfaces. h)
description: Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt. | Ivmdisplay-_GenerateThumbnail Methode (vpccominterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail-Methode Virtual PC
- _GenerateThumbnail-Methode Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, _GenerateThumbnail-Methode
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366414"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="ae36b-107">Ivmdisplay:: \_ generatethumschlag bnail-Methode</span><span class="sxs-lookup"><span data-stu-id="ae36b-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="ae36b-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae36b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ae36b-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ae36b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ae36b-110">Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae36b-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae36b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae36b-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="ae36b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae36b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae36b-113">*thumbnailimage* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae36b-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae36b-114">Das Array von Pixeln, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae36b-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae36b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae36b-115">Return value</span></span>

<span data-ttu-id="ae36b-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ae36b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ae36b-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ae36b-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ae36b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae36b-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ae36b-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ae36b-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ae36b-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae36b-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ae36b-121"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ae36b-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ae36b-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ae36b-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ae36b-123"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ae36b-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ae36b-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ae36b-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ae36b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae36b-125">Remarks</span></span>

<span data-ttu-id="ae36b-126">Diese Schnittstelle gibt die Miniaturansicht effizienter als die [**Miniatur**](ivmdisplay-thumbnail.md) Ansichts Eigenschaft zurück, kann aber nicht von Skript Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae36b-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="ae36b-127">Die Miniaturansicht ist immer 64 Pixel breit und 48 Pixel hoch.</span><span class="sxs-lookup"><span data-stu-id="ae36b-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="ae36b-128">Jedes Pixel ist 32 Bits, wobei die oberen 8 Bits den blauen Wert des Pixels darstellen, die nächsten 8 Bits den grünen Wert des Pixels darstellen und die nächsten 8 Bits den roten Wert des Pixels darstellen.</span><span class="sxs-lookup"><span data-stu-id="ae36b-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="ae36b-129">Die ersten 64 Elemente im Array sind die erste Zeile der Miniaturansicht, die nächsten 64 Elemente sind die zweite Zeile usw.</span><span class="sxs-lookup"><span data-stu-id="ae36b-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="ae36b-130">Diese Methode gibt ein statisches Array von Pixeln zurück, das effizienter ist als die Rückgabe eines **SAFEARRAY** von **Variant** -Werten, aber nicht mit Skript Clients kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ae36b-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae36b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae36b-131">Requirements</span></span>



| <span data-ttu-id="ae36b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae36b-132">Requirement</span></span> | <span data-ttu-id="ae36b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ae36b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae36b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae36b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ae36b-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae36b-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae36b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae36b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ae36b-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ae36b-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ae36b-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ae36b-138">End of client support</span></span><br/>    | <span data-ttu-id="ae36b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae36b-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ae36b-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="ae36b-140">Product</span></span><br/>                  | <span data-ttu-id="ae36b-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ae36b-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ae36b-142">Header</span><span class="sxs-lookup"><span data-stu-id="ae36b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae36b-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae36b-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ae36b-144">IID</span><span class="sxs-lookup"><span data-stu-id="ae36b-144">IID</span></span><br/>                      | <span data-ttu-id="ae36b-145">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="ae36b-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ae36b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae36b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae36b-147">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="ae36b-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

