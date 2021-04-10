---
title: Ivmvirtualpc getfloppydiskimagetype-Methode (vpccominterfaces. h)
description: Ruft den Typ einer vorhandenen Disketten Image Datei ab.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Getfloppydiskimagetype-Methode Virtual PC
- Getfloppydiskimagetype-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getfloppydiskimagetype-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106041"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="23565-106">Ivmvirtualpc:: getfloppydiskimagetype-Methode</span><span class="sxs-lookup"><span data-stu-id="23565-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="23565-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23565-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="23565-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="23565-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="23565-109">Ruft den Typ einer vorhandenen Disketten Image Datei ab.</span><span class="sxs-lookup"><span data-stu-id="23565-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="23565-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="23565-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="23565-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="23565-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23565-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23565-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23565-113">Der vollständige Pfad zur Abbild Datei des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="23565-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="23565-114">*ImageType* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="23565-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="23565-115">Der Typ des Datenträger Images.</span><span class="sxs-lookup"><span data-stu-id="23565-115">The disk image type.</span></span> <span data-ttu-id="23565-116">Eine Liste der Werte finden Sie unter [**vmfloppydiskimagetype**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="23565-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23565-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23565-117">Return value</span></span>

<span data-ttu-id="23565-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23565-118">This method can return one of these values.</span></span>



| <span data-ttu-id="23565-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="23565-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="23565-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23565-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23565-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23565-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="23565-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="23565-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="23565-123"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="23565-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="23565-124">Der *ImagePath* -Parameter oder der *ImageType* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="23565-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="23565-125"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="23565-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="23565-126">Das System kann die durch den *ImagePath* -Parameter angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="23565-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="23565-127"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="23565-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="23565-128">Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="23565-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="23565-129"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="23565-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="23565-130">Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="23565-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="23565-131"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="23565-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="23565-132">Der *ImagePath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="23565-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="23565-133">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23565-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="23565-134"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="23565-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="23565-135">Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="23565-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="23565-136">Die Länge des Pfads muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="23565-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="23565-137"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="23565-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="23565-138">Die von *ImagePath* angegebene Datei ist kein Diskettenbild, oder es ist ein unerwarteter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="23565-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="23565-139"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="23565-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="23565-140">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="23565-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="23565-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23565-141">Requirements</span></span>



| <span data-ttu-id="23565-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23565-142">Requirement</span></span> | <span data-ttu-id="23565-143">Wert</span><span class="sxs-lookup"><span data-stu-id="23565-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23565-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23565-144">Minimum supported client</span></span><br/> | <span data-ttu-id="23565-145">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23565-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23565-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23565-146">Minimum supported server</span></span><br/> | <span data-ttu-id="23565-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="23565-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="23565-148">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="23565-148">End of client support</span></span><br/>    | <span data-ttu-id="23565-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23565-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="23565-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="23565-150">Product</span></span><br/>                  | <span data-ttu-id="23565-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="23565-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="23565-152">Header</span><span class="sxs-lookup"><span data-stu-id="23565-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="23565-153"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="23565-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="23565-154">IID</span><span class="sxs-lookup"><span data-stu-id="23565-154">IID</span></span><br/>                      | <span data-ttu-id="23565-155">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="23565-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="23565-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23565-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23565-157">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="23565-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

