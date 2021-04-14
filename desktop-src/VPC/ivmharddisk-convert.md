---
title: Ivmharddisk Convert-Methode (vpccominterfaces. h)
description: Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Konvertieren von Virtual PC-Methoden
- Convert-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Methode konvertieren
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478804"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="e886f-106">Ivmharddisk:: Convert-Methode</span><span class="sxs-lookup"><span data-stu-id="e886f-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="e886f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e886f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e886f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e886f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e886f-109">Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="e886f-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="e886f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e886f-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="e886f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e886f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e886f-112">*converteddiskimagepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e886f-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e886f-113">Der Pfad zur Ziel-Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="e886f-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="e886f-114">*converteddiskimagetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e886f-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e886f-115">Der Typ des Ziel Datenträger Images.</span><span class="sxs-lookup"><span data-stu-id="e886f-115">The type of the target disk image.</span></span> <span data-ttu-id="e886f-116">Eine Liste der Werte finden Sie unter [**vmharddisktype**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="e886f-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="e886f-117">*converttask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e886f-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e886f-118">Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen des Abschlusses des Konvertierungsprozesses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e886f-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e886f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e886f-119">Return value</span></span>

<span data-ttu-id="e886f-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e886f-120">This method can return one of these values.</span></span>



| <span data-ttu-id="e886f-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e886f-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="e886f-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e886f-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e886f-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="e886f-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e886f-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="e886f-125"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="e886f-126">Der *converteddiskimagepath* -Parameter ist leer, oder die VHD-Erweiterung für den Dateinamen fehlt.</span><span class="sxs-lookup"><span data-stu-id="e886f-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e886f-127"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="e886f-128">Ein Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e886f-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="e886f-129"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="e886f-130">Das System kann den vom *converteddiskimagepath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="e886f-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="e886f-131"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="e886f-132">Der *converteddiskimagepath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="e886f-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="e886f-133"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="e886f-134">Der *converteddiskimagepath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="e886f-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="e886f-135">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e886f-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="e886f-136"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="e886f-137">Der vom *converteddiskimagepath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="e886f-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="e886f-138">Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="e886f-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="e886f-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="e886f-140">Entweder wird die virtuelle Festplatte verwendet, auf die von diesem Objekt verwiesen wird, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="e886f-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="e886f-141"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="e886f-142">Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um diese virtuelle Festplatte zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e886f-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e886f-143"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="e886f-144">Die Datei, auf die vom *converteddiskimagepath* -Parameter verwiesen wird, ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e886f-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e886f-145"><dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="e886f-146">Der *converteddiskimagepath* -Parameter muss entweder " **vmdisktype \_ Dynamic** " oder " **vmdisktype \_ FixedSize**" lauten.</span><span class="sxs-lookup"><span data-stu-id="e886f-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="e886f-147"><dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="e886f-148">Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, scheint kein gültiges Image zu sein.</span><span class="sxs-lookup"><span data-stu-id="e886f-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="e886f-149"><dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="e886f-150">Das übergeordnete Element der virtuellen Festplatte, auf die von diesem Objekt verwiesen wird, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e886f-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e886f-151"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="e886f-152">Das Image der virtuellen Festplatte kann nicht konvertiert werden, da die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="e886f-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e886f-153"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="e886f-154">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e886f-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e886f-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e886f-155">Remarks</span></span>

<span data-ttu-id="e886f-156">Die Quelldatei bleibt nach dem Konvertierungs Vorgang intakt.</span><span class="sxs-lookup"><span data-stu-id="e886f-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="e886f-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e886f-157">Requirements</span></span>



| <span data-ttu-id="e886f-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e886f-158">Requirement</span></span> | <span data-ttu-id="e886f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="e886f-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e886f-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e886f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="e886f-161">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e886f-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e886f-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e886f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="e886f-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e886f-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e886f-164">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e886f-164">End of client support</span></span><br/>    | <span data-ttu-id="e886f-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e886f-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e886f-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="e886f-166">Product</span></span><br/>                  | <span data-ttu-id="e886f-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e886f-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e886f-168">Header</span><span class="sxs-lookup"><span data-stu-id="e886f-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="e886f-169"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e886f-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e886f-170">IID</span><span class="sxs-lookup"><span data-stu-id="e886f-170">IID</span></span><br/>                      | <span data-ttu-id="e886f-171">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="e886f-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="e886f-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e886f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e886f-173">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="e886f-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

