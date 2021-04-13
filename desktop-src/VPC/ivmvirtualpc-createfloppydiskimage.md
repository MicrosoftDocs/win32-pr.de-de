---
title: Ivmvirtualpc-Methode "deatefloppydiskimage" ("vpccominterfaces. h")
description: Erstellt eine Disketten Image Datei.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Methode "" der Methode "kreatefloppydiskimage"
- Methode "die Methode" für den virtuellen PC der Methode "" mit der Methode "ivmvirtualpc"
- Ivmvirtualpc Interface Virtual PC, Methode "kreatefloppydiskimage"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478150"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="e4a62-106">Ivmvirtualpc:: kreatefloppydiskimage-Methode</span><span class="sxs-lookup"><span data-stu-id="e4a62-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="e4a62-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e4a62-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4a62-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e4a62-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4a62-109">Erstellt eine Disketten Image Datei.</span><span class="sxs-lookup"><span data-stu-id="e4a62-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a62-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a62-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="e4a62-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4a62-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a62-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4a62-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a62-113">Der vollständige Pfad zur neuen Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="e4a62-113">The full path to the new disk image file.</span></span> <span data-ttu-id="e4a62-114">Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4a62-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e4a62-115">*ImageType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4a62-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a62-116">Der Typ des zu erstellenden Disketten Bilds.</span><span class="sxs-lookup"><span data-stu-id="e4a62-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="e4a62-117">Nur **vmfloppydiskimage \_ lowdensity** (1) und **vmfloppydiskimage \_ highdensity** (2) werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4a62-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="e4a62-118">Siehe [**vmfloppydiskimagetype**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="e4a62-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a62-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4a62-119">Return value</span></span>

<span data-ttu-id="e4a62-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e4a62-120">This method can return one of these values.</span></span>



| <span data-ttu-id="e4a62-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e4a62-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="e4a62-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4a62-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4a62-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="e4a62-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4a62-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="e4a62-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="e4a62-126">Der *ImagePath* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e4a62-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="e4a62-127"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="e4a62-128">Der *ImageType* -Parameter ist nicht [**vmfloppydiskimage \_ lowdensity**](vmfloppydiskimagetype.md) (1) oder **vmfloppydiskimage \_ highdensity** (2).</span><span class="sxs-lookup"><span data-stu-id="e4a62-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="e4a62-129"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="e4a62-130">Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="e4a62-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="e4a62-131"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="e4a62-132">Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="e4a62-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e4a62-133"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="e4a62-134">Der *ImagePath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="e4a62-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="e4a62-135">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e4a62-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="e4a62-136"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="e4a62-137">Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="e4a62-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="e4a62-138">Die Länge des Pfads muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="e4a62-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="e4a62-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="e4a62-140">Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e4a62-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="e4a62-141"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="e4a62-142">Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um das virtuelle Disketten Image zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4a62-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e4a62-143"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="e4a62-144">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e4a62-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="e4a62-145"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="e4a62-146">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="e4a62-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="e4a62-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4a62-147">Requirements</span></span>



| <span data-ttu-id="e4a62-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4a62-148">Requirement</span></span> | <span data-ttu-id="e4a62-149">Wert</span><span class="sxs-lookup"><span data-stu-id="e4a62-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a62-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4a62-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a62-151">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4a62-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4a62-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4a62-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a62-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e4a62-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e4a62-154">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e4a62-154">End of client support</span></span><br/>    | <span data-ttu-id="e4a62-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4a62-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e4a62-156">Produkt</span><span class="sxs-lookup"><span data-stu-id="e4a62-156">Product</span></span><br/>                  | <span data-ttu-id="e4a62-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4a62-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e4a62-158">Header</span><span class="sxs-lookup"><span data-stu-id="e4a62-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a62-159"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a62-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e4a62-160">IID</span><span class="sxs-lookup"><span data-stu-id="e4a62-160">IID</span></span><br/>                      | <span data-ttu-id="e4a62-161">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="e4a62-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e4a62-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4a62-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a62-163">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="e4a62-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

