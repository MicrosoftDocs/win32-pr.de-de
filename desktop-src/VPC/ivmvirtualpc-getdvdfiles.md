---
title: Ivmvirtualpc getdvdfiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter DVD-Dateien ab.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Getdvdfiles-Methode Virtual PC
- Getdvdfiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getdvdfiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342643"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a><span data-ttu-id="e13f9-106">Ivmvirtualpc:: getdvdfiles-Methode</span><span class="sxs-lookup"><span data-stu-id="e13f9-106">IVMVirtualPC::GetDVDFiles method</span></span>

<span data-ttu-id="e13f9-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e13f9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e13f9-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e13f9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e13f9-109">Ruft ein Array bekannter DVD-Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="e13f9-109">Retrieves an array of known DVD files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13f9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e13f9-110">Syntax</span></span>


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a><span data-ttu-id="e13f9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e13f9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13f9-112">*inadditionalsearchpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e13f9-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13f9-113">Diese Pfade werden zusammen mit den Pfaden durchsucht, die in der [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) -Eigenschaft festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e13f9-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="e13f9-114">*outdvdfilelist* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e13f9-114">*outDVDFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e13f9-115">Ein Array von virtuellen DVD-Dateien, die in den angegebenen Suchpfaden gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e13f9-115">An array of virtual DVD files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13f9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e13f9-116">Return value</span></span>

<span data-ttu-id="e13f9-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e13f9-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e13f9-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e13f9-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e13f9-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e13f9-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e13f9-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e13f9-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e13f9-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e13f9-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e13f9-123">Der *outdvdfilelist* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e13f9-123">The *outDVDFileList* parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e13f9-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="e13f9-125">Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e13f9-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="e13f9-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e13f9-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e13f9-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e13f9-128"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e13f9-129">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="e13f9-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e13f9-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e13f9-130">Remarks</span></span>

<span data-ttu-id="e13f9-131">Die Suchpfade, die zum Abrufen des Arrays von Dateien verwendet werden, [**enthalten zusätzlich zu**](ivmvirtualpc-searchpaths.md) den durch den *inadditionalsearchpath* -Parameter angegebenen und den installerspeicherort für das Integrations Komponenten Modul festgelegte.</span><span class="sxs-lookup"><span data-stu-id="e13f9-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13f9-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e13f9-132">Requirements</span></span>



| <span data-ttu-id="e13f9-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e13f9-133">Requirement</span></span> | <span data-ttu-id="e13f9-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e13f9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13f9-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e13f9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e13f9-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e13f9-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e13f9-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e13f9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e13f9-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e13f9-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e13f9-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e13f9-139">End of client support</span></span><br/>    | <span data-ttu-id="e13f9-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e13f9-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e13f9-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="e13f9-141">Product</span></span><br/>                  | <span data-ttu-id="e13f9-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e13f9-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e13f9-143">Header</span><span class="sxs-lookup"><span data-stu-id="e13f9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13f9-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13f9-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e13f9-145">IID</span><span class="sxs-lookup"><span data-stu-id="e13f9-145">IID</span></span><br/>                      | <span data-ttu-id="e13f9-146">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="e13f9-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e13f9-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e13f9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13f9-148">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="e13f9-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

