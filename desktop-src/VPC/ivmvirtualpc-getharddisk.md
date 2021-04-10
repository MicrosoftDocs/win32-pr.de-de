---
title: Ivmvirtualpc getharddisk-Methode (vpccominterfaces. h)
description: Ruft ein Objekt ab, das einer vorhandenen Datenträger Image Datei entspricht.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Getharddisk-Methode Virtual PC
- Getharddisk-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getharddisk-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956950"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="55ae2-106">Ivmvirtualpc:: getharddisk-Methode</span><span class="sxs-lookup"><span data-stu-id="55ae2-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="55ae2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55ae2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="55ae2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="55ae2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="55ae2-109">Ruft ein Objekt ab, das einer vorhandenen Datenträger Image Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="55ae2-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ae2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="55ae2-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="55ae2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="55ae2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ae2-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55ae2-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ae2-113">Der vollständige Pfad zu einer vorhandenen Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="55ae2-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="55ae2-114">*Festplatte* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="55ae2-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="55ae2-115">Ein [**ivmharddisk**](ivmharddisk.md) -Objekt, das diesem Datenträger Image entspricht.</span><span class="sxs-lookup"><span data-stu-id="55ae2-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ae2-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55ae2-116">Return value</span></span>

<span data-ttu-id="55ae2-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="55ae2-117">This method can return one of these values.</span></span>



| <span data-ttu-id="55ae2-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="55ae2-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="55ae2-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55ae2-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55ae2-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="55ae2-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="55ae2-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="55ae2-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="55ae2-123">Der *ImagePath* -oder *Harddisk* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="55ae2-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="55ae2-124"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="55ae2-125">Das System kann die durch den *ImagePath* -Parameter angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="55ae2-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="55ae2-126"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="55ae2-127">Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="55ae2-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="55ae2-128"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="55ae2-129">Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="55ae2-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="55ae2-130"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="55ae2-131">Der *ImagePath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="55ae2-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="55ae2-132">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="55ae2-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="55ae2-133"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="55ae2-134">Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="55ae2-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="55ae2-135">Die Länge des Pfads muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="55ae2-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="55ae2-136"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="55ae2-137">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="55ae2-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="55ae2-138"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="55ae2-139">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="55ae2-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="55ae2-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55ae2-140">Requirements</span></span>



| <span data-ttu-id="55ae2-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55ae2-141">Requirement</span></span> | <span data-ttu-id="55ae2-142">Wert</span><span class="sxs-lookup"><span data-stu-id="55ae2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ae2-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55ae2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="55ae2-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55ae2-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55ae2-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55ae2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="55ae2-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="55ae2-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="55ae2-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="55ae2-147">End of client support</span></span><br/>    | <span data-ttu-id="55ae2-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55ae2-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="55ae2-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="55ae2-149">Product</span></span><br/>                  | <span data-ttu-id="55ae2-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55ae2-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="55ae2-151">Header</span><span class="sxs-lookup"><span data-stu-id="55ae2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="55ae2-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ae2-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="55ae2-153">IID</span><span class="sxs-lookup"><span data-stu-id="55ae2-153">IID</span></span><br/>                      | <span data-ttu-id="55ae2-154">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="55ae2-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="55ae2-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55ae2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ae2-156">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="55ae2-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

