---
title: Ivmvirtualpc-Methode "kreatedifferencingvirtualharddisk" (vpccominterfaces. h)
description: Erstellt eine differenzierende virtuelle Festplatte.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Methode "kreatedifferencingvirtualharddisk" Virtual PC
- "\"Kreatedifferencingvirtualharddisk\"-Methode Virtual PC, ivmvirtualpc-Schnittstelle"
- Ivmvirtualpc Interface Virtual PC, Methode "kreatedifferencingvirtualharddisk"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344093"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="ff4db-106">Ivmvirtualpc:: kreatedifferencingvirtualharddisk-Methode</span><span class="sxs-lookup"><span data-stu-id="ff4db-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="ff4db-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff4db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff4db-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff4db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff4db-109">Erstellt eine differenzierende virtuelle Festplatte.</span><span class="sxs-lookup"><span data-stu-id="ff4db-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4db-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff4db-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="ff4db-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff4db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff4db-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff4db-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4db-113">Der Pfad zur neuen Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="ff4db-113">The path to the new disk image file.</span></span> <span data-ttu-id="ff4db-114">Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ff4db-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="ff4db-115">Element *Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff4db-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4db-116">Der Pfad zur Datei für den übergeordneten Datenträger Image.</span><span class="sxs-lookup"><span data-stu-id="ff4db-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="ff4db-117">*disktask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ff4db-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4db-118">Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff4db-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff4db-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff4db-119">Return value</span></span>

<span data-ttu-id="ff4db-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ff4db-120">This method can return one of these values.</span></span>



| <span data-ttu-id="ff4db-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ff4db-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="ff4db-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff4db-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff4db-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="ff4db-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff4db-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ff4db-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="ff4db-126">Ein Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ff4db-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ff4db-127"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="ff4db-128">Das System kann den durch den Parameter " *ImagePath* " oder " *Parameter Path"* angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="ff4db-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="ff4db-129"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ Laufwerk)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="ff4db-130">Die durch den *ImagePath* -Parameter angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="ff4db-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="ff4db-131"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="ff4db-132">Der Parameter " *ImagePath* " oder "Parameter *path* " enthält ein ungültiges Zeichen (" \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="ff4db-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="ff4db-133"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="ff4db-134">Sowohl der *ImagePath* -Parameter als auch der Parameter *Parameter Path geben* einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="ff4db-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="ff4db-135">Mindestens einer der Parameter muss ein absoluter Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="ff4db-136"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="ff4db-137">Der von den Parametern " *ImagePath* " oder "Parameter *path* " angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="ff4db-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="ff4db-138">Die Länge des Pfads muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="ff4db-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="ff4db-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="ff4db-140">Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ff4db-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="ff4db-141"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="ff4db-142">Für das dynamisch erweiterbare virtuelle Festplatten Abbild sind mindestens 8 MB freier Speicherplatz auf dem Host Volume erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ff4db-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="ff4db-143"><dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ groß**</dt> <dt>0xa0040683</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="ff4db-144">Die Parameter *Größe* muss kleiner als 2.088.960 MB sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="ff4db-145">Wenn das Format "FAT16" ist, muss die Größe kleiner als 2000 MB sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="ff4db-146"><dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ klein**</dt> <dt>0xa0040684</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="ff4db-147">Nicht formatierte und FAT16 formatierte virtuelle Festplatten Abbilder müssen mindestens 3 MB groß sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="ff4db-148">Auf FAT32 formatierte virtuelle Festplatten Abbilder müssen mindestens 514 MB groß sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="ff4db-149"><dt>**VM \_ E- \_ Datei \_ zu \_ groß \_ für \_ Volume**</dt> <dt>0xa0040679</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="ff4db-150">Die Größe der Datei kann vom Hostvolume nicht unterstützt werden, wenn das Image der dynamisch erweiterbaren virtuellen Festplatte auf den vollständigen Grenzwert erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="ff4db-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="ff4db-151">Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB.</span><span class="sxs-lookup"><span data-stu-id="ff4db-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="ff4db-152">Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.</span><span class="sxs-lookup"><span data-stu-id="ff4db-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="ff4db-153"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="ff4db-154">Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff4db-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="ff4db-155"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="ff4db-156">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="ff4db-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="ff4db-157"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ff4db-158">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ff4db-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ff4db-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff4db-159">Remarks</span></span>

<span data-ttu-id="ff4db-160">Obwohl *es sich bei* entweder um *ImagePath* oder um einen relativen Pfad handeln kann, muss mindestens einer der Pfade ein absoluter Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="ff4db-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="ff4db-161">Wenn ein Pfad Parameter ein relativer Pfad ist, wird davon ausgegangen, dass er relativ zum anderen path-Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="ff4db-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4db-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff4db-162">Requirements</span></span>



| <span data-ttu-id="ff4db-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff4db-163">Requirement</span></span> | <span data-ttu-id="ff4db-164">Wert</span><span class="sxs-lookup"><span data-stu-id="ff4db-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4db-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff4db-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4db-166">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff4db-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff4db-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff4db-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4db-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff4db-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff4db-169">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ff4db-169">End of client support</span></span><br/>    | <span data-ttu-id="ff4db-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff4db-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff4db-171">Produkt</span><span class="sxs-lookup"><span data-stu-id="ff4db-171">Product</span></span><br/>                  | <span data-ttu-id="ff4db-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff4db-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff4db-173">Header</span><span class="sxs-lookup"><span data-stu-id="ff4db-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff4db-174"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff4db-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff4db-175">IID</span><span class="sxs-lookup"><span data-stu-id="ff4db-175">IID</span></span><br/>                      | <span data-ttu-id="ff4db-176">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="ff4db-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ff4db-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff4db-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4db-178">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="ff4db-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

