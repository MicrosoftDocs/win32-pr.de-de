---
title: Ivmguestos getosversioninfo-Methode (vpccominterfaces. h)
description: Ruft Versionsinformationen für das Gast Betriebssystem ab, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Getosversioninfo-Methode Virtual PC
- Getosversioninfo-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, getosversioninfo-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346337"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="f8d21-106">Ivmguestos:: getosversioninfo-Methode</span><span class="sxs-lookup"><span data-stu-id="f8d21-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="f8d21-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8d21-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f8d21-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f8d21-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f8d21-109">Ruft Versionsinformationen für das Gast Betriebssystem ab, das auf dem virtuellen Computer (VM) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8d21-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d21-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8d21-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f8d21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8d21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d21-112">*guestosversioninfo* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f8d21-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d21-113">Ein Zeiger auf eine [**guestosversioninfoex**](guestosversioninfoex.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f8d21-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d21-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8d21-114">Return value</span></span>

<span data-ttu-id="f8d21-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f8d21-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f8d21-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f8d21-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f8d21-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8d21-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8d21-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8d21-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="f8d21-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8d21-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f8d21-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f8d21-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="f8d21-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f8d21-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f8d21-122"><dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="f8d21-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="f8d21-123">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f8d21-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="f8d21-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f8d21-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="f8d21-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f8d21-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="f8d21-126"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="f8d21-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="f8d21-127">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8d21-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f8d21-128"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="f8d21-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="f8d21-129">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="f8d21-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="f8d21-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8d21-130">Requirements</span></span>



| <span data-ttu-id="f8d21-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8d21-131">Requirement</span></span> | <span data-ttu-id="f8d21-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f8d21-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d21-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8d21-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d21-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8d21-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8d21-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8d21-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d21-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8d21-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f8d21-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f8d21-137">End of client support</span></span><br/>    | <span data-ttu-id="f8d21-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8d21-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f8d21-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="f8d21-139">Product</span></span><br/>                  | <span data-ttu-id="f8d21-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f8d21-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f8d21-141">Header</span><span class="sxs-lookup"><span data-stu-id="f8d21-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8d21-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d21-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f8d21-143">IID</span><span class="sxs-lookup"><span data-stu-id="f8d21-143">IID</span></span><br/>                      | <span data-ttu-id="f8d21-144">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="f8d21-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f8d21-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8d21-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d21-146">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="f8d21-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

