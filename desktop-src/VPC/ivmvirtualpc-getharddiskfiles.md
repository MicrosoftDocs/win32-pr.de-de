---
title: Ivmvirtualpc getharddiskfiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter virtueller Festplatten Dateien ab.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Getharddiskfiles-Methode Virtual PC
- Getharddiskfiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getharddiskfiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4162ae2667d389b445f44973c89a60fafd4c772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518785"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a><span data-ttu-id="071ce-106">Ivmvirtualpc:: getharddiskfiles-Methode</span><span class="sxs-lookup"><span data-stu-id="071ce-106">IVMVirtualPC::GetHardDiskFiles method</span></span>

<span data-ttu-id="071ce-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="071ce-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="071ce-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="071ce-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="071ce-109">Ruft ein Array bekannter virtueller Festplatten Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="071ce-109">Retrieves an array of known virtual hard disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="071ce-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="071ce-110">Syntax</span></span>


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="071ce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="071ce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="071ce-112">*inadditionalsearchpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="071ce-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071ce-113">Diese Pfade werden zusammen mit den Pfaden durchsucht, die in der [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) -Eigenschaft festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="071ce-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="071ce-114">*outharddiskfilelist* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="071ce-114">*outHardDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="071ce-115">Ein Array von Pfad Zeichenfolgen für die virtuellen Festplatten Dateien, die in den angegebenen Suchpfaden gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="071ce-115">An array of path strings for the virtual hard disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="071ce-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="071ce-116">Return value</span></span>

<span data-ttu-id="071ce-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="071ce-117">This method can return one of these values.</span></span>



| <span data-ttu-id="071ce-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="071ce-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="071ce-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="071ce-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="071ce-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="071ce-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="071ce-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="071ce-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="071ce-123">Der *outharddiskfilelist* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="071ce-123">The *outHardDiskFileList* parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="071ce-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="071ce-125">Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="071ce-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="071ce-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="071ce-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="071ce-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="071ce-128"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="071ce-129">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="071ce-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="071ce-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="071ce-130">Remarks</span></span>

<span data-ttu-id="071ce-131">Die Suchpfade, die zum Abrufen des Arrays von Dateien verwendet werden, enthalten zusätzlich zu den vom *inadditionalsearchpath* -Parameter festgelegten Suchpfaden die zuvor von [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) festgelegten Pfade.</span><span class="sxs-lookup"><span data-stu-id="071ce-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="071ce-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="071ce-132">Requirements</span></span>



| <span data-ttu-id="071ce-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="071ce-133">Requirement</span></span> | <span data-ttu-id="071ce-134">Wert</span><span class="sxs-lookup"><span data-stu-id="071ce-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="071ce-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="071ce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="071ce-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="071ce-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="071ce-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="071ce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="071ce-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="071ce-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="071ce-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="071ce-139">End of client support</span></span><br/>    | <span data-ttu-id="071ce-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="071ce-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="071ce-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="071ce-141">Product</span></span><br/>                  | <span data-ttu-id="071ce-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="071ce-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="071ce-143">Header</span><span class="sxs-lookup"><span data-stu-id="071ce-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="071ce-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="071ce-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="071ce-145">IID</span><span class="sxs-lookup"><span data-stu-id="071ce-145">IID</span></span><br/>                      | <span data-ttu-id="071ce-146">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="071ce-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="071ce-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="071ce-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071ce-148">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="071ce-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

