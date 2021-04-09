---
title: Ivmdisplay videomode-Eigenschaft (vpccominterfaces. h)
description: Ruft den aktuellen Videomodus ab.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Videomode-Eigenschaft virtueller PC
- Videomode-Eigenschaft virtueller PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, videomode (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956421"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="fce76-106">Ivmdisplay:: videomode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fce76-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="fce76-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fce76-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fce76-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fce76-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fce76-109">Ruft den aktuellen Videomodus ab.</span><span class="sxs-lookup"><span data-stu-id="fce76-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="fce76-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fce76-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce76-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce76-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="fce76-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fce76-112">Property value</span></span>

<span data-ttu-id="fce76-113">Der aktuelle Videomodus des Gast Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="fce76-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="fce76-114">Eine Liste der Werte finden Sie unter [**vmdisplayvideomode**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="fce76-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="fce76-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fce76-115">Error codes</span></span>



| <span data-ttu-id="fce76-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="fce76-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="fce76-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fce76-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fce76-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fce76-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fce76-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fce76-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="fce76-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="fce76-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fce76-122"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="fce76-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="fce76-123">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fce76-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="fce76-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="fce76-125">Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fce76-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="fce76-126"><dt>VM \_ E \_ keine \_ Anzeige</dt> <dt>0xa0040850</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="fce76-127">Für den virtuellen Computer kann keine gültige Anzeige gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="fce76-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="fce76-128"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fce76-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fce76-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="fce76-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fce76-130">Requirements</span></span>



| <span data-ttu-id="fce76-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fce76-131">Requirement</span></span> | <span data-ttu-id="fce76-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fce76-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce76-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fce76-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fce76-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fce76-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fce76-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fce76-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fce76-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fce76-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fce76-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fce76-137">End of client support</span></span><br/>    | <span data-ttu-id="fce76-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fce76-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fce76-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="fce76-139">Product</span></span><br/>                  | <span data-ttu-id="fce76-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fce76-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fce76-141">Header</span><span class="sxs-lookup"><span data-stu-id="fce76-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce76-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce76-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fce76-143">IID</span><span class="sxs-lookup"><span data-stu-id="fce76-143">IID</span></span><br/>                      | <span data-ttu-id="fce76-144">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="fce76-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fce76-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fce76-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce76-146">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="fce76-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

