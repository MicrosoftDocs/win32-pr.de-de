---
title: Ivmvirtualpc getfloppydiskfiles-Methode (vpccominterfaces. h)
description: Ruft ein Array bekannter virtueller Disketten Dateien ab.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Getfloppydiskfiles-Methode Virtual PC
- Getfloppydiskfiles-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getfloppydiskfiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743441"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a><span data-ttu-id="fd504-106">Ivmvirtualpc:: getfloppydiskfiles-Methode</span><span class="sxs-lookup"><span data-stu-id="fd504-106">IVMVirtualPC::GetFloppyDiskFiles method</span></span>

<span data-ttu-id="fd504-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fd504-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd504-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd504-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd504-109">Ruft ein Array bekannter virtueller Disketten Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="fd504-109">Retrieves an array of known virtual floppy disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd504-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd504-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="fd504-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd504-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd504-112">*inadditionalsearchpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd504-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd504-113">Diese Pfade werden zusammen mit den Pfaden durchsucht, die in der [**ivmvirtualpc:: SearchPath**](ivmvirtualpc-searchpaths.md) -Eigenschaft festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fd504-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="fd504-114">*outfloppydiskfilelist* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fd504-114">*outFloppyDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fd504-115">Ein Array von virtuellen Disketten Dateien, die in den angegebenen Suchpfaden gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="fd504-115">An array of virtual floppy disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd504-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd504-116">Return value</span></span>

<span data-ttu-id="fd504-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fd504-117">This method can return one of these values.</span></span>



| <span data-ttu-id="fd504-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="fd504-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="fd504-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd504-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd504-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="fd504-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd504-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fd504-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="fd504-123">Der *outfloppydiskfilelist* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="fd504-123">The *outFloppyDiskFileList* parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fd504-124"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="fd504-125">Der *inadditionalsearchpath* -Parameter ist kein Array von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="fd504-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="fd504-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="fd504-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fd504-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="fd504-128"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="fd504-129">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="fd504-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd504-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd504-130">Remarks</span></span>

<span data-ttu-id="fd504-131">Die Suchpfade, die zum Abrufen des Arrays von Dateien verwendet werden, [**enthalten zusätzlich zu**](ivmvirtualpc-searchpaths.md) den durch den *inadditionalsearchpath* -Parameter angegebenen und den installerspeicherort für das Integrations Komponenten Modul festgelegte.</span><span class="sxs-lookup"><span data-stu-id="fd504-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd504-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd504-132">Requirements</span></span>



| <span data-ttu-id="fd504-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd504-133">Requirement</span></span> | <span data-ttu-id="fd504-134">Wert</span><span class="sxs-lookup"><span data-stu-id="fd504-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd504-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd504-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fd504-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd504-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd504-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd504-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fd504-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd504-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd504-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="fd504-139">End of client support</span></span><br/>    | <span data-ttu-id="fd504-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd504-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd504-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="fd504-141">Product</span></span><br/>                  | <span data-ttu-id="fd504-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd504-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd504-143">Header</span><span class="sxs-lookup"><span data-stu-id="fd504-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd504-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd504-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd504-145">IID</span><span class="sxs-lookup"><span data-stu-id="fd504-145">IID</span></span><br/>                      | <span data-ttu-id="fd504-146">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="fd504-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fd504-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd504-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd504-148">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="fd504-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

