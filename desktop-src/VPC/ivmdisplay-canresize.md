---
title: Ivmdisplay CanResize-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der Gast Auflösungs Änderungen zulässt.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- CanResize-Eigenschaft virtueller PC
- CanResize Property Virtual PC, ivmdisplay Interface
- Ivmdisplay Interface Virtual PC, CanResize-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743472"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="651c4-106">Ivmdisplay:: CanResize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="651c4-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="651c4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="651c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="651c4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="651c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="651c4-109">Bestimmt, ob der Gast Auflösungs Änderungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="651c4-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="651c4-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="651c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="651c4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="651c4-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="651c4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="651c4-112">Property value</span></span>

<span data-ttu-id="651c4-113">**Variant \_ TRUE** , wenn der Gast Auflösungs Änderungen zulässt, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="651c4-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="651c4-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="651c4-114">Error codes</span></span>



| <span data-ttu-id="651c4-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="651c4-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="651c4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="651c4-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="651c4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="651c4-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="651c4-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="651c4-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="651c4-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="651c4-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="651c4-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="651c4-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="651c4-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="651c4-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="651c4-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="651c4-124">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="651c4-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="651c4-125"><dt>VM \_ E \_ keine \_ Anzeige</dt> <dt>0xa0040850</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="651c4-126">Für den virtuellen Computer wurde kein Videogerät gefunden.</span><span class="sxs-lookup"><span data-stu-id="651c4-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="651c4-127"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="651c4-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="651c4-128">Die Funktion "Integrations Komponenten" ist nicht verfügbar. entweder sind die Integrations Komponenten nicht installiert, oder das Feature wurde deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="651c4-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="651c4-129"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="651c4-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="651c4-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="651c4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="651c4-131">Requirements</span></span>



| <span data-ttu-id="651c4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="651c4-132">Requirement</span></span> | <span data-ttu-id="651c4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="651c4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="651c4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="651c4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="651c4-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="651c4-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="651c4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="651c4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="651c4-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="651c4-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="651c4-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="651c4-138">End of client support</span></span><br/>    | <span data-ttu-id="651c4-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="651c4-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="651c4-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="651c4-140">Product</span></span><br/>                  | <span data-ttu-id="651c4-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="651c4-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="651c4-142">Header</span><span class="sxs-lookup"><span data-stu-id="651c4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="651c4-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="651c4-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="651c4-144">IID</span><span class="sxs-lookup"><span data-stu-id="651c4-144">IID</span></span><br/>                      | <span data-ttu-id="651c4-145">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="651c4-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="651c4-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="651c4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651c4-147">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="651c4-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

