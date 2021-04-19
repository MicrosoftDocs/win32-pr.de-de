---
title: Ivmvirtualmachine AddHardDiskConnection-Methode (vpccominterfaces. h)
description: Fügt der virtuellen Maschine eine neue Festplatten Verbindung hinzu.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection-Methode Virtual PC
- AddHardDiskConnection-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, AddHardDiskConnection-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338344"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="b462e-106">Ivmvirtualmachine:: AddHardDiskConnection-Methode</span><span class="sxs-lookup"><span data-stu-id="b462e-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="b462e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b462e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b462e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b462e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b462e-109">Fügt der virtuellen Maschine (VM) eine neue Festplatten Verbindung hinzu.</span><span class="sxs-lookup"><span data-stu-id="b462e-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b462e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b462e-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="b462e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b462e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b462e-112">*harddiskpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b462e-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b462e-113">Der vollständige Pfad der VHD-Datei (Virtual Hard Disk) zum Herstellen einer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b462e-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="b462e-114">*Busnummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b462e-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b462e-115">Der Bus, an den das Laufwerk angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b462e-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="b462e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b462e-116">Value</span></span>                                                                        | <span data-ttu-id="b462e-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b462e-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="b462e-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b462e-119">Das Laufwerk wird an den ersten Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="b462e-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="b462e-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b462e-121">Das Laufwerk wird an den zweiten Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="b462e-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b462e-122">*devicengegen ber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b462e-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b462e-123">Das Gerät, an das das Laufwerk angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b462e-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="b462e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b462e-124">Value</span></span>                                                                        | <span data-ttu-id="b462e-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b462e-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b462e-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b462e-127">Das Laufwerk wird an das erste Gerät auf dem Bus angefügt.</span><span class="sxs-lookup"><span data-stu-id="b462e-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="b462e-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b462e-129">Das Laufwerk wird mit dem zweiten Gerät auf dem Bus verbunden.</span><span class="sxs-lookup"><span data-stu-id="b462e-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b462e-130">*harddiskconnection* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b462e-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b462e-131">Ein [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b462e-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b462e-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b462e-132">Return value</span></span>

<span data-ttu-id="b462e-133">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b462e-133">This method can return one of these values.</span></span>



| <span data-ttu-id="b462e-134">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b462e-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="b462e-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b462e-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b462e-136"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="b462e-137">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b462e-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="b462e-138"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="b462e-139">Der *harddiskconnection* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b462e-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b462e-140"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="b462e-141">Der Parameter " *harddiskpath* " ist **null** , oder der Parameter " *busnumber* " oder " *devicenenumber* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b462e-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b462e-142"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="b462e-143">Das System kann die durch den *harddiskpath* -Parameter angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="b462e-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="b462e-144"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="b462e-145">Das System kann den durch den *harddiskpath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="b462e-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="b462e-146"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="b462e-147">Der *harddiskpath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="b462e-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b462e-148"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="b462e-149">Der *harddiskpath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="b462e-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b462e-150">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b462e-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="b462e-151"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="b462e-152">Der durch den *harddiskpath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="b462e-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="b462e-153">Der Pfad muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="b462e-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b462e-154"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="b462e-155">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b462e-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="b462e-156"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="b462e-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="b462e-157">Der virtuelle Computer befindet sich in einem laufenden oder gespeicherten Zustand.</span><span class="sxs-lookup"><span data-stu-id="b462e-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="b462e-158"><dt>**VM \_ E \_ Drive \_ Bus \_ loc \_ \_ verwendet**</dt> <dt>0xa00400503</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="b462e-159">Der angegebene Busspeicherort wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="b462e-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="b462e-160"><dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="b462e-161">Die VHD ist größer als 127 GB und kann nicht mit dem IDE-Bus verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="b462e-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="b462e-162"><dt>**VM \_ E \_ nicht unterstützter \_ \_ Festplatten \_ Datenträger**</dt> <dt>0xa00400686</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="b462e-163">Der *harddiskpath* -Parameter verweist auf eine verknüpfte VHD oder eine differenzierende VHD zu einer verknüpften VHD.</span><span class="sxs-lookup"><span data-stu-id="b462e-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="b462e-164">Verknüpfte VHDs können nicht an virtuelle Computer angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b462e-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="b462e-165"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="b462e-166">Die angegebene VHD ist bereits mit einem anderen Busspeicherort für diesen virtuellen Computer verbunden.</span><span class="sxs-lookup"><span data-stu-id="b462e-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="b462e-167"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="b462e-168">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b462e-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b462e-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b462e-169">Remarks</span></span>

<span data-ttu-id="b462e-170">Sie können einem beendeten virtuellen Computer nur eine neue Festplatten Verbindung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b462e-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b462e-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b462e-171">Requirements</span></span>



| <span data-ttu-id="b462e-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b462e-172">Requirement</span></span> | <span data-ttu-id="b462e-173">Wert</span><span class="sxs-lookup"><span data-stu-id="b462e-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b462e-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b462e-174">Minimum supported client</span></span><br/> | <span data-ttu-id="b462e-175">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b462e-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b462e-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b462e-176">Minimum supported server</span></span><br/> | <span data-ttu-id="b462e-177">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b462e-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b462e-178">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b462e-178">End of client support</span></span><br/>    | <span data-ttu-id="b462e-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b462e-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b462e-180">Produkt</span><span class="sxs-lookup"><span data-stu-id="b462e-180">Product</span></span><br/>                  | <span data-ttu-id="b462e-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b462e-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b462e-182">Header</span><span class="sxs-lookup"><span data-stu-id="b462e-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="b462e-183"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b462e-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b462e-184">IID</span><span class="sxs-lookup"><span data-stu-id="b462e-184">IID</span></span><br/>                      | <span data-ttu-id="b462e-185">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="b462e-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b462e-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b462e-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b462e-187">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="b462e-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

