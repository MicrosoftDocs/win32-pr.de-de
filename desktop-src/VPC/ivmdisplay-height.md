---
title: Ivmdisplay Height-Eigenschaft (vpccominterfaces. h)
description: Höhe der Anzeige des virtuellen Computers in Pixel.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Height-Eigenschaft virtueller PC
- Height-Eigenschaft Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, Height-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040680"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="82e2d-106">Ivmdisplay:: Height-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82e2d-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="82e2d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82e2d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82e2d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82e2d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82e2d-109">Ruft die Höhe der Anzeige des virtuellen Computers in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="82e2d-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="82e2d-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="82e2d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e2d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="82e2d-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="82e2d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="82e2d-112">Property value</span></span>

<span data-ttu-id="82e2d-113">Die Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="82e2d-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82e2d-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="82e2d-114">Error codes</span></span>



| <span data-ttu-id="82e2d-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="82e2d-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="82e2d-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82e2d-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82e2d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="82e2d-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="82e2d-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="82e2d-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="82e2d-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="82e2d-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="82e2d-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="82e2d-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="82e2d-122">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="82e2d-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="82e2d-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="82e2d-124">Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82e2d-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="82e2d-125"><dt>VM \_ E \_ keine \_ Anzeige</dt> <dt>0xa0040850</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="82e2d-126">Für den virtuellen Computer kann keine gültige Anzeige gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="82e2d-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="82e2d-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="82e2d-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="82e2d-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="82e2d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82e2d-129">Requirements</span></span>



| <span data-ttu-id="82e2d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82e2d-130">Requirement</span></span> | <span data-ttu-id="82e2d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="82e2d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e2d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82e2d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="82e2d-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82e2d-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82e2d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82e2d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="82e2d-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="82e2d-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82e2d-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="82e2d-136">End of client support</span></span><br/>    | <span data-ttu-id="82e2d-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82e2d-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82e2d-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="82e2d-138">Product</span></span><br/>                  | <span data-ttu-id="82e2d-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82e2d-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82e2d-140">Header</span><span class="sxs-lookup"><span data-stu-id="82e2d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="82e2d-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82e2d-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82e2d-142">IID</span><span class="sxs-lookup"><span data-stu-id="82e2d-142">IID</span></span><br/>                      | <span data-ttu-id="82e2d-143">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="82e2d-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="82e2d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82e2d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e2d-145">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="82e2d-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

