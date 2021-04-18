---
title: Ivmmouse usingabsolutekoordinaten-Eigenschaft (vpccominterfaces. h)
description: Ruft ab, ob Maus Koordinaten absolute oder relative Koordinaten darstellen.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Usingabsolutekoordinaten-Eigenschaft virtueller PC
- Usingabsolutekoordinaten-Eigenschaft Virtual PC, ivmmouse-Schnittstelle
- Ivmmouse Interface Virtual PC, usingabsolutekoordinaten (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518713"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="f2e46-106">Ivmmouse:: usingabsolutekoordinaten (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f2e46-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="f2e46-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2e46-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2e46-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2e46-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2e46-109">Ruft ab, ob Maus Koordinaten absolute oder relative Koordinaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="f2e46-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="f2e46-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f2e46-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e46-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e46-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="f2e46-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f2e46-112">Property value</span></span>

<span data-ttu-id="f2e46-113">**Variant \_ TRUE** , wenn das Mausgerät für die Verwendung absoluter Koordinaten festgelegt werden soll, **Variant \_ false** , um relative Koordinaten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2e46-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2e46-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f2e46-114">Error codes</span></span>



| <span data-ttu-id="f2e46-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f2e46-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f2e46-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2e46-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2e46-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2e46-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f2e46-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2e46-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="f2e46-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f2e46-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="f2e46-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f2e46-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f2e46-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="f2e46-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f2e46-122">Der virtuelle Computer, an den dieses Mausgerät angefügt ist, wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2e46-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="f2e46-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="f2e46-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f2e46-124">Integrations Komponenten sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f2e46-124">Integration components are not installed.</span></span> <span data-ttu-id="f2e46-125">Integrations Komponenten sind erforderlich, um absolute Koordinaten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2e46-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="f2e46-126"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f2e46-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f2e46-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f2e46-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="f2e46-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2e46-128">Remarks</span></span>

<span data-ttu-id="f2e46-129">Diese Eigenschaft ist nur für dieses Objekt lokal und wird standardmäßig für ein neues [**ivmmouse**](ivmmouse.md) -Objekt **Variant \_ false** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2e46-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="f2e46-130">Beachten Sie, dass Integrations Komponenten installiert werden müssen, um absolute Koordinaten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2e46-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e46-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2e46-131">Requirements</span></span>



| <span data-ttu-id="f2e46-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2e46-132">Requirement</span></span> | <span data-ttu-id="f2e46-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f2e46-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e46-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2e46-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e46-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2e46-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2e46-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2e46-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e46-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f2e46-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2e46-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f2e46-138">End of client support</span></span><br/>    | <span data-ttu-id="f2e46-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2e46-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2e46-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="f2e46-140">Product</span></span><br/>                  | <span data-ttu-id="f2e46-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2e46-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2e46-142">Header</span><span class="sxs-lookup"><span data-stu-id="f2e46-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e46-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e46-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2e46-144">IID</span><span class="sxs-lookup"><span data-stu-id="f2e46-144">IID</span></span><br/>                      | <span data-ttu-id="f2e46-145">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="f2e46-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="f2e46-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2e46-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e46-147">**Ivmmouse**</span><span class="sxs-lookup"><span data-stu-id="f2e46-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

