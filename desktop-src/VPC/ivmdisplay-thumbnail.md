---
title: Ivmdisplay-Miniatur Ansichts Eigenschaft (vpccominterfaces. h)
description: Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt. | Ivmdisplay-Miniatur Ansichts Eigenschaft (vpccominterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Miniatur Ansichts Eigenschaft Virtual PC
- Miniatur Ansichts Eigenschaft Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, Miniatur Ansichts Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961285"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="e7bf3-107">Ivmdisplay:: Miniaturansicht (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="e7bf3-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e7bf3-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e7bf3-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e7bf3-110">Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="e7bf3-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bf3-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7bf3-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="e7bf3-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7bf3-113">Property value</span></span>

<span data-ttu-id="e7bf3-114">Eine Variante vom Typ VT \_ array \| VT \_ mit Einträgen vom Typ VT \_ UI4, eine für jedes Pixel in der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e7bf3-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e7bf3-115">Error codes</span></span>



| <span data-ttu-id="e7bf3-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e7bf3-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e7bf3-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e7bf3-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e7bf3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e7bf3-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e7bf3-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e7bf3-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e7bf3-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf3-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e7bf3-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7bf3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7bf3-124">Remarks</span></span>

<span data-ttu-id="e7bf3-125">Diese Schnittstelle gibt die Miniaturansicht weniger effizient als die [**\_ generatethrebnail**](ivmdisplay--generatethumbnail.md) -Methode zurück, kann aber von Skript Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="e7bf3-126">Die Miniaturansicht ist immer 64 Pixel breit und 48 Pixel hoch.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="e7bf3-127">Jedes Pixel ist 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="e7bf3-128">Die ersten 64 Elemente im Array sind die erste Zeile der Pixel in der Miniaturansicht, die nächsten 64 Elemente sind die zweite Zeile usw.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bf3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7bf3-129">Requirements</span></span>



| <span data-ttu-id="e7bf3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7bf3-130">Requirement</span></span> | <span data-ttu-id="e7bf3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e7bf3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bf3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bf3-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7bf3-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7bf3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bf3-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e7bf3-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e7bf3-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e7bf3-136">End of client support</span></span><br/>    | <span data-ttu-id="e7bf3-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7bf3-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7bf3-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="e7bf3-138">Product</span></span><br/>                  | <span data-ttu-id="e7bf3-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e7bf3-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e7bf3-140">Header</span><span class="sxs-lookup"><span data-stu-id="e7bf3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7bf3-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf3-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e7bf3-142">IID</span><span class="sxs-lookup"><span data-stu-id="e7bf3-142">IID</span></span><br/>                      | <span data-ttu-id="e7bf3-143">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="e7bf3-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e7bf3-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7bf3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bf3-145">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="e7bf3-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

