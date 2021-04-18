---
title: Ivmguestos isuserloggedon-Methode (vpccominterfaces. h)
description: Bestimmt, ob die angeforderte Sitzung vorhanden ist.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Isuserloggedon-Methode virtueller PC
- Isuserloggedon-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, isuserloggedon-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340971"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="6f039-106">Ivmguestos:: isuserloggedon-Methode</span><span class="sxs-lookup"><span data-stu-id="6f039-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="6f039-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f039-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6f039-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6f039-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6f039-109">Bestimmt, ob die angeforderte Sitzung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6f039-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f039-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f039-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="6f039-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f039-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f039-112">*inrailsession* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f039-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f039-113">Legen Sie für eine Rail-Sitzung auf 0 oder für eine RDP-Sitzung den Wert 1 fest.</span><span class="sxs-lookup"><span data-stu-id="6f039-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="6f039-114">*outsessionpresent* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6f039-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6f039-115">Auf **Variant \_ true** festgelegt, wenn die Sitzung vorhanden ist, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="6f039-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f039-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f039-116">Return value</span></span>

<span data-ttu-id="6f039-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6f039-117">This method can return one of these values.</span></span>



| <span data-ttu-id="6f039-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="6f039-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="6f039-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f039-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f039-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="6f039-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f039-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6f039-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="6f039-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6f039-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6f039-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="6f039-125">Der *outsessionpresent* -Parameter ist ungültig oder **null**.</span><span class="sxs-lookup"><span data-stu-id="6f039-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="6f039-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="6f039-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6f039-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="6f039-128"><dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="6f039-129">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6f039-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="6f039-130"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="6f039-131">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="6f039-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="6f039-132"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="6f039-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="6f039-133">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6f039-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="6f039-134"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="6f039-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="6f039-135">Das Feature "Integrations Komponenten" ist auf dieser VM nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6f039-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="6f039-136"><dt>**VM \_ E- \_ VM \_ angeh**</dt> alten <dt>0xa00400507</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="6f039-137">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="6f039-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="6f039-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f039-138">Requirements</span></span>



| <span data-ttu-id="6f039-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f039-139">Requirement</span></span> | <span data-ttu-id="6f039-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6f039-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f039-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f039-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6f039-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f039-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f039-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f039-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6f039-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6f039-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6f039-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6f039-145">End of client support</span></span><br/>    | <span data-ttu-id="6f039-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f039-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6f039-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="6f039-147">Product</span></span><br/>                  | <span data-ttu-id="6f039-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6f039-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6f039-149">Header</span><span class="sxs-lookup"><span data-stu-id="6f039-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f039-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f039-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6f039-151">IID</span><span class="sxs-lookup"><span data-stu-id="6f039-151">IID</span></span><br/>                      | <span data-ttu-id="6f039-152">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="6f039-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6f039-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f039-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f039-154">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="6f039-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

