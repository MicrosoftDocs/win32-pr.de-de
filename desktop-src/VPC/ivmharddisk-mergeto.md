---
title: Ivmharddisk mergeto-Methode (vpccominterfaces. h)
description: Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen zusammen.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Mergeto-Methode virtueller PC
- Mergeto-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, mergeto-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103965"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="2f915-106">Ivmharddisk:: mergeto-Methode</span><span class="sxs-lookup"><span data-stu-id="2f915-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="2f915-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f915-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f915-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f915-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f915-109">Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen (bis einschließlich der übergeordneten virtuellen Festplatte) einer neuen Festplatten Datei zusammen.</span><span class="sxs-lookup"><span data-stu-id="2f915-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f915-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f915-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="2f915-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f915-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f915-112">*newdiskimagepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f915-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f915-113">Der Pfad zum neuen Ziel Datenträger Image, in dem die ausgewählten Datenträger Images zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2f915-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="2f915-114">*newdiskimagetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f915-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f915-115">Der Typ des neuen Ziel datenträgerbilds.</span><span class="sxs-lookup"><span data-stu-id="2f915-115">The type of new target disk image.</span></span> <span data-ttu-id="2f915-116">Die für das neue Ziel Datenträgerabbild zulässigen Abbild Typen sind " **vmdisktype \_ Dynamic** " und " **vmdisktype \_ FixedSize**".</span><span class="sxs-lookup"><span data-stu-id="2f915-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="2f915-117">Weitere Informationen finden Sie unter [**vmharddisktype**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="2f915-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f915-118">*mergetask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f915-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f915-119">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Zusammenführungs Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="2f915-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f915-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f915-120">Return value</span></span>

<span data-ttu-id="2f915-121">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2f915-121">This method can return one of these values.</span></span>



| <span data-ttu-id="2f915-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2f915-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="2f915-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f915-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f915-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="2f915-125">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f915-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="2f915-126"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="2f915-127">Ein Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2f915-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="2f915-128"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="2f915-129">Der *newdiskimagepath* -Parameter ist leer.</span><span class="sxs-lookup"><span data-stu-id="2f915-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2f915-130"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="2f915-131">Das System kann die durch den Parameter " *newdiskimagepath* " angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="2f915-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="2f915-132"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="2f915-133">Das System kann den durch den *newdiskimagepath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="2f915-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="2f915-134"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="2f915-135">Der *newdiskimagepath* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="2f915-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="2f915-136"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="2f915-137">Der *newdiskimagepath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="2f915-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="2f915-138">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f915-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="2f915-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="2f915-140">Der durch den *newdiskimagepath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="2f915-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="2f915-141">Der Pfad muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="2f915-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="2f915-142"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="2f915-143">Entweder wird die virtuelle Festplatte verwendet, auf die von diesem Objekt verwiesen wird, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f915-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="2f915-144"><dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="2f915-145">Dieser Fehler ist darauf zurückzuführen, dass es sich bei dem virtuellen Festplatten Image, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, nicht um ein differenzierender Datenträger Image handelt oder weil der *newdiskimagetype* -Parameter nicht zu den zulässigen Werten, **vmdisktype \_ Dynamic** oder **vmdisktype \_ FixedSize** gehört.</span><span class="sxs-lookup"><span data-stu-id="2f915-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="2f915-146"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="2f915-147">Die Datei, auf die der *newdiskimagepath* -Parameter verweist, ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2f915-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2f915-148"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="2f915-149">Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um diese virtuelle Festplatte zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="2f915-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="2f915-150"><dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="2f915-151">Das übergeordnete Element der virtuellen Festplatte, auf die von diesem Objekt verwiesen wird, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2f915-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="2f915-152"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="2f915-153">Das virtuelle Festplatten Abbild kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="2f915-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="2f915-154"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="2f915-155">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2f915-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="2f915-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f915-156">Requirements</span></span>



| <span data-ttu-id="2f915-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f915-157">Requirement</span></span> | <span data-ttu-id="2f915-158">Wert</span><span class="sxs-lookup"><span data-stu-id="2f915-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f915-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f915-159">Minimum supported client</span></span><br/> | <span data-ttu-id="2f915-160">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f915-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f915-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f915-161">Minimum supported server</span></span><br/> | <span data-ttu-id="2f915-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f915-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f915-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2f915-163">End of client support</span></span><br/>    | <span data-ttu-id="2f915-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f915-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f915-165">Produkt</span><span class="sxs-lookup"><span data-stu-id="2f915-165">Product</span></span><br/>                  | <span data-ttu-id="2f915-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f915-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f915-167">Header</span><span class="sxs-lookup"><span data-stu-id="2f915-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f915-168"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f915-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f915-169">IID</span><span class="sxs-lookup"><span data-stu-id="2f915-169">IID</span></span><br/>                      | <span data-ttu-id="2f915-170">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="2f915-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2f915-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f915-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f915-172">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="2f915-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

