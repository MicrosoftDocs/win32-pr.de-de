---
title: Ivmdisplay Width-Eigenschaft (vpccominterfaces. h)
description: Breite der VM-Anzeige in Pixel.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Width Property Virtual PC
- Width-Eigenschaft Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, Width-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518803"
---
# <a name="ivmdisplaywidth-property"></a><span data-ttu-id="dda66-106">Ivmdisplay:: Width-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dda66-106">IVMDisplay::Width property</span></span>

<span data-ttu-id="dda66-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dda66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dda66-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dda66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dda66-109">Ruft die Breite der Anzeige des virtuellen Computers (VM) in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="dda66-109">Retrieves the width of the virtual machine's (VM's) display, in pixels.</span></span>

<span data-ttu-id="dda66-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dda66-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda66-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dda66-111">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a><span data-ttu-id="dda66-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dda66-112">Property value</span></span>

<span data-ttu-id="dda66-113">Die Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="dda66-113">The width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dda66-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dda66-114">Error codes</span></span>



| <span data-ttu-id="dda66-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="dda66-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="dda66-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dda66-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dda66-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="dda66-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="dda66-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dda66-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="dda66-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="dda66-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dda66-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="dda66-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="dda66-122">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="dda66-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="dda66-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="dda66-124">Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dda66-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="dda66-125"><dt>VM \_ E \_ keine \_ Anzeige</dt> <dt>0xa0040850</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="dda66-126">Für den virtuellen Computer kann keine gültige Anzeige gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="dda66-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="dda66-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="dda66-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="dda66-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="dda66-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dda66-129">Requirements</span></span>



| <span data-ttu-id="dda66-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dda66-130">Requirement</span></span> | <span data-ttu-id="dda66-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dda66-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda66-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dda66-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dda66-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dda66-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dda66-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dda66-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dda66-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dda66-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dda66-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="dda66-136">End of client support</span></span><br/>    | <span data-ttu-id="dda66-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dda66-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dda66-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="dda66-138">Product</span></span><br/>                  | <span data-ttu-id="dda66-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dda66-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dda66-140">Header</span><span class="sxs-lookup"><span data-stu-id="dda66-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda66-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda66-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dda66-142">IID</span><span class="sxs-lookup"><span data-stu-id="dda66-142">IID</span></span><br/>                      | <span data-ttu-id="dda66-143">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="dda66-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="dda66-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dda66-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda66-145">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="dda66-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

