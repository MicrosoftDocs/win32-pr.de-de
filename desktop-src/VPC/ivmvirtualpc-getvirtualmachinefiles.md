---
title: Ivmvirtualpc getvirtualmachinefiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter Konfigurationsdateien für virtuelle Maschinen ab.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Getvirtualmachinefiles-Methode virtueller PC
- Getvirtualmachinefiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getvirtualmachinefiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341227"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="fe086-106">Ivmvirtualpc:: getvirtualmachinefiles-Methode</span><span class="sxs-lookup"><span data-stu-id="fe086-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="fe086-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe086-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fe086-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fe086-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fe086-109">Ruft ein Array bekannter Konfigurationsdateien für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="fe086-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe086-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe086-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="fe086-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe086-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe086-112">*inadditionalsearchpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe086-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe086-113">Diese Pfade werden zusammen mit den Pfaden durchsucht, die in den Eigenschaften [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) und [**ivmvirtualpc::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fe086-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="fe086-114">*inexcluddregisteredvms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe086-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe086-115">**True** , wenn registrierte virtuelle Computer aus dem Array ausgeschlossen werden sollen, wenn der *outvirtualmachinefilelist* -Parameter zurückgegeben wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="fe086-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe086-116">*outvirtualmachinefilelist* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fe086-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fe086-117">Ein Array von Pfad Zeichenfolgen für die Konfigurationsdateien der virtuellen Maschine, die in den angegebenen Suchpfaden gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="fe086-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe086-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe086-118">Return value</span></span>

<span data-ttu-id="fe086-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fe086-119">This method can return one of these values.</span></span>



| <span data-ttu-id="fe086-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="fe086-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="fe086-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe086-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe086-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="fe086-123">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe086-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fe086-124"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="fe086-125">Der *outvirtualmachinefilelist* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="fe086-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="fe086-126"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="fe086-127">Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fe086-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="fe086-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="fe086-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fe086-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="fe086-130"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="fe086-131">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="fe086-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe086-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe086-132">Remarks</span></span>

<span data-ttu-id="fe086-133">Die Suchpfade, die zum Abrufen des Arrays von Konfigurationsdateien verwendet werden, enthalten diejenigen, die zuvor von [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) und [**ivmvirtualpc::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegt wurden, zusätzlich zu den vom *inadditionalsearchpath* -Parameter angegebenen.</span><span class="sxs-lookup"><span data-stu-id="fe086-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe086-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe086-134">Requirements</span></span>



| <span data-ttu-id="fe086-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe086-135">Requirement</span></span> | <span data-ttu-id="fe086-136">Wert</span><span class="sxs-lookup"><span data-stu-id="fe086-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe086-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe086-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fe086-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe086-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe086-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe086-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fe086-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe086-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fe086-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fe086-141">End of client support</span></span><br/>    | <span data-ttu-id="fe086-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe086-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fe086-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="fe086-143">Product</span></span><br/>                  | <span data-ttu-id="fe086-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fe086-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fe086-145">Header</span><span class="sxs-lookup"><span data-stu-id="fe086-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe086-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe086-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fe086-147">IID</span><span class="sxs-lookup"><span data-stu-id="fe086-147">IID</span></span><br/>                      | <span data-ttu-id="fe086-148">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="fe086-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fe086-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe086-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe086-150">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="fe086-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

