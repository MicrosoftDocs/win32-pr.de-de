---
title: Ivmvirtualpc-Methode "deatefixedvirtualharddisk" (vpccominterfaces. h)
description: Erstellt eine virtuelle Festplatte mit fester Größe.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Methode "" für den virtuellen PC
- Methode "kreatefixedvirtualharddisk" Virtual PC, ivmvirtualpc
- Ivmvirtualpc Interface Virtual PC, Methode "kreatefixedvirtualharddisk"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103959"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a><span data-ttu-id="51bd4-106">Ivmvirtualpc:: deatefixedvirtualharddisk-Methode</span><span class="sxs-lookup"><span data-stu-id="51bd4-106">IVMVirtualPC::CreateFixedVirtualHardDisk method</span></span>

<span data-ttu-id="51bd4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51bd4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51bd4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="51bd4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="51bd4-109">Erstellt eine virtuelle Festplatte mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="51bd4-109">Creates a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bd4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="51bd4-110">Syntax</span></span>


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="51bd4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="51bd4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51bd4-112">*ImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51bd4-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51bd4-113">Der vollständige Pfad zur neuen Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="51bd4-113">The full path to the new disk image file.</span></span> <span data-ttu-id="51bd4-114">Der enthaltende Ordner wird erstellt, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="51bd4-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="51bd4-115">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51bd4-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51bd4-116">Die Größe des Bilds in Megabyte.</span><span class="sxs-lookup"><span data-stu-id="51bd4-116">The size, in megabytes, of the image.</span></span> <span data-ttu-id="51bd4-117">Die maximale Größe beträgt 2.088.960 MB (2040gb).</span><span class="sxs-lookup"><span data-stu-id="51bd4-117">Maximum size is 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="51bd4-118">*disktask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="51bd4-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="51bd4-119">Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen der Image Erstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51bd4-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51bd4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51bd4-120">Return value</span></span>

<span data-ttu-id="51bd4-121">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="51bd4-121">This method can return one of these values.</span></span>



| <span data-ttu-id="51bd4-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="51bd4-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="51bd4-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51bd4-123">Description</span></span>                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51bd4-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="51bd4-125">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="51bd4-125">The operation was successful.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="51bd4-126"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="51bd4-127">Ein Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51bd4-127">A parameter is **NULL**.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="51bd4-128"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="51bd4-129">Der *size* -Parameter ist kleiner oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="51bd4-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="51bd4-130"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="51bd4-131">Das System kann den durch den *ImagePath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="51bd4-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="51bd4-132"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ Laufwerk)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="51bd4-133">Die durch den *ImagePath* -Parameter angegebene Datei befindet sich auf einer CD-ROM oder DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="51bd4-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="51bd4-134"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="51bd4-135">Der *ImagePath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="51bd4-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="51bd4-136"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="51bd4-137">Sowohl der *ImagePath* -Parameter gibt einen leeren als auch einen relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="51bd4-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="51bd4-138">Mindestens einer der Parameter muss ein absoluter Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-138">At least one of the parameters must be an absolute path.</span></span><br/>                         |
| <dl> <span data-ttu-id="51bd4-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="51bd4-140">Der durch den *ImagePath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="51bd4-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="51bd4-141">Die Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-141">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/>                |
| <dl> <span data-ttu-id="51bd4-142"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="51bd4-143">Die Datei, auf die der *ImagePath* -Parameter verweist, ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="51bd4-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="51bd4-144"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="51bd4-145">Für das dynamisch erweiterbare virtuelle Festplatten Abbild sind mindestens 8 MB freier Speicherplatz auf dem Host Volume erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51bd4-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="51bd4-146"><dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ groß**</dt> <dt>0xa0040683</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="51bd4-147">Der *size* -Parameter muss kleiner als 2.088.960 MB sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-147">The *size* parameter must be less than 2,088,960 MB.</span></span> <span data-ttu-id="51bd4-148">Wenn das Format "FAT16" ist, muss der *size* -Parameter kleiner als 2000 MB sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-148">If the format is FAT16, then the *size* parameter must be less than 2000 MB.</span></span><br/>                    |
| <dl> <span data-ttu-id="51bd4-149"><dt>**VM \_ E- \_ Abbild \_ Größe \_ zu \_ klein**</dt> <dt>0xa0040684</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="51bd4-150">Nicht formatierte und FAT16 formatierte virtuelle Festplatten Abbilder müssen mindestens 3 MB groß sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="51bd4-151">Auf FAT32 formatierte virtuelle Festplatten Abbilder müssen mindestens 514 MB groß sein.</span><span class="sxs-lookup"><span data-stu-id="51bd4-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>    |
| <dl> <span data-ttu-id="51bd4-152"><dt>**VM \_ E- \_ Datei \_ zu \_ groß \_ für \_ Volume**</dt> <dt>0xa0040679</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="51bd4-153">Die Größe der Datei kann vom Hostvolume nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51bd4-153">The host volume cannot support a file this size.</span></span> <span data-ttu-id="51bd4-154">Die maximale Dateigröße für ein FAT32-Volume beträgt 4 GB.</span><span class="sxs-lookup"><span data-stu-id="51bd4-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="51bd4-155">Die maximale Dateigröße für ein FAT16-Volume beträgt 2 GB.</span><span class="sxs-lookup"><span data-stu-id="51bd4-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="51bd4-156"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="51bd4-157">Die virtuelle Festplatte kann nicht erstellt werden, nachdem das Herunterfahren der Anwendung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="51bd4-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="51bd4-158"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="51bd4-159">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="51bd4-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="51bd4-160"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="51bd4-161">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="51bd4-161">An unexpected error has occurred.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="51bd4-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51bd4-162">Requirements</span></span>



| <span data-ttu-id="51bd4-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51bd4-163">Requirement</span></span> | <span data-ttu-id="51bd4-164">Wert</span><span class="sxs-lookup"><span data-stu-id="51bd4-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bd4-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51bd4-165">Minimum supported client</span></span><br/> | <span data-ttu-id="51bd4-166">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51bd4-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51bd4-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51bd4-167">Minimum supported server</span></span><br/> | <span data-ttu-id="51bd4-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="51bd4-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="51bd4-169">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="51bd4-169">End of client support</span></span><br/>    | <span data-ttu-id="51bd4-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51bd4-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51bd4-171">Produkt</span><span class="sxs-lookup"><span data-stu-id="51bd4-171">Product</span></span><br/>                  | <span data-ttu-id="51bd4-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="51bd4-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="51bd4-173">Header</span><span class="sxs-lookup"><span data-stu-id="51bd4-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="51bd4-174"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="51bd4-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="51bd4-175">IID</span><span class="sxs-lookup"><span data-stu-id="51bd4-175">IID</span></span><br/>                      | <span data-ttu-id="51bd4-176">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="51bd4-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="51bd4-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51bd4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bd4-178">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="51bd4-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

