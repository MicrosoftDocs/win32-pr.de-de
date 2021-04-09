---
title: Ivmmouse-HorizontalPosition-Eigenschaft (vpccominterfaces. h)
description: Absolute x-Koordinate der Maus.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- HorizontalPosition-Eigenschaft virtueller PC
- HorizontalPosition-Eigenschaft Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, HorizontalPosition (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8506ad0d4583b9829ca2b1832686d32e67ded261
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957119"
---
# <a name="ivmmousehorizontalposition-property"></a><span data-ttu-id="477f6-106">Ivmmouse:: HorizontalPosition (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="477f6-106">IVMMouse::HorizontalPosition property</span></span>

<span data-ttu-id="477f6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="477f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="477f6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="477f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="477f6-109">Ruft die absolute x-Koordinate der Maus ab.</span><span class="sxs-lookup"><span data-stu-id="477f6-109">Retrieves the absolute x-coordinate of the mouse.</span></span>

<span data-ttu-id="477f6-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="477f6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="477f6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="477f6-111">Syntax</span></span>


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="477f6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="477f6-112">Property value</span></span>

<span data-ttu-id="477f6-113">Die x-Koordinate, die die neue Position der Maus angibt.</span><span class="sxs-lookup"><span data-stu-id="477f6-113">The x-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="477f6-114">Wenn Sie absolute Koordinaten verwenden, gibt dieser Wert die neue x-Koordinate der Maus an.</span><span class="sxs-lookup"><span data-stu-id="477f6-114">When using absolute coordinates, this value specifies the new x-coordinate of the mouse.</span></span> <span data-ttu-id="477f6-115">Wenn relative Koordinaten verwendet werden, gibt dieser Wert die Anzahl der Pixel an, die die Maus in der x-Richtung verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="477f6-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the x direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="477f6-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="477f6-116">Error codes</span></span>



| <span data-ttu-id="477f6-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="477f6-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="477f6-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="477f6-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="477f6-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="477f6-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="477f6-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="477f6-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="477f6-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="477f6-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="477f6-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="477f6-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="477f6-124">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="477f6-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="477f6-125"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="477f6-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="477f6-126">Integrations Komponenten müssen installiert sein, um die Mausposition abzurufen, oder die Mausposition bei der Verwendung absoluter Koordinaten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="477f6-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="477f6-127"><dt>VM \_ E \_ verwenden \_ relativer \_ Koordinaten</dt> <dt>0xa0040802</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="477f6-128">Das Mausgerät ist derzeit auf die Verwendung relativer Maus Koordinaten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="477f6-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="477f6-129"><dt>VM \_ E \_ Maus \_ nicht \_ aktiv</dt> <dt>0xa0040800</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="477f6-130">Die absoluten Koordinaten können nicht abgerufen werden, wenn das Mausgerät nicht eingeschaltet ist oder wenn es auf dem virtuellen Computer zurzeit nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="477f6-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="477f6-131"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="477f6-132">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="477f6-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="477f6-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="477f6-133">Remarks</span></span>

<span data-ttu-id="477f6-134">Diese Eigenschaft kann nicht abgerufen werden, wenn relative Koordinaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="477f6-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="477f6-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="477f6-135">Requirements</span></span>



| <span data-ttu-id="477f6-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="477f6-136">Requirement</span></span> | <span data-ttu-id="477f6-137">Wert</span><span class="sxs-lookup"><span data-stu-id="477f6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="477f6-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="477f6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="477f6-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="477f6-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="477f6-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="477f6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="477f6-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="477f6-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="477f6-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="477f6-142">End of client support</span></span><br/>    | <span data-ttu-id="477f6-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="477f6-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="477f6-144">Produkt</span><span class="sxs-lookup"><span data-stu-id="477f6-144">Product</span></span><br/>                  | <span data-ttu-id="477f6-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="477f6-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="477f6-146">Header</span><span class="sxs-lookup"><span data-stu-id="477f6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="477f6-147"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="477f6-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="477f6-148">IID</span><span class="sxs-lookup"><span data-stu-id="477f6-148">IID</span></span><br/>                      | <span data-ttu-id="477f6-149">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="477f6-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="477f6-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="477f6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="477f6-151">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="477f6-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

