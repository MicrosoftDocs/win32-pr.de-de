---
title: Ivmvirtualpc-Methode "kreatevirtualmachine" (vpccominterfaces. h)
description: Erstellt eine neue Konfiguration für virtuelle Maschinen und ruft das Objekt der virtuellen Maschine ab.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Der Methode "Virtual PC" der Methode "die Methode"
- Die Methode "Virtual PC" der Methode "ivmvirtualmachine", ivmvirtualpc
- Ivmvirtualpc Interface Virtual PC, Methode "kreatevirtualmachine"
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478153"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="41697-106">Ivmvirtualpc:: kreatevirtualmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="41697-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="41697-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41697-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="41697-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="41697-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="41697-109">Erstellt eine neue Konfiguration für virtuelle Maschinen und ruft das Objekt der virtuellen Maschine ab.</span><span class="sxs-lookup"><span data-stu-id="41697-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41697-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="41697-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="41697-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="41697-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41697-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41697-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41697-113">Der Name des zu erstellenden virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="41697-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="41697-114">Die Länge des Namens darf nicht länger als 80 Zeichen sein, und die kombinierte Länge des Namens und des Pfads zu VMC-und vmcx-Dateien darf **maximal \_** zulässige (260) Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="41697-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="41697-115">Die Dateinamen Erweiterungen. vmc und. vmcx werden an das Ende des Namens der virtuellen Maschine angehängt, wenn die Konfigurationsdateien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="41697-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="41697-116">Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, muss der *ConfigurationPath* -Parameter den vollständigen Pfad zur VMC-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="41697-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="41697-117">*ConfigurationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41697-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41697-118">Der Pfad zu dem Ordner, der die VMC-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="41697-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="41697-119">Dieser Ordner wird erstellt, wenn er nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41697-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="41697-120">Wenn *ConfigurationName* **null** oder eine leere Zeichenfolge ist, muss der vollständige Pfad der neuen Konfigurationsdatei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41697-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="41697-121">*virtualmachine* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="41697-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="41697-122">Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="41697-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41697-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41697-123">Return value</span></span>

<span data-ttu-id="41697-124">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="41697-124">This method can return one of these values.</span></span>



| <span data-ttu-id="41697-125">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="41697-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="41697-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41697-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41697-127"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="41697-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="41697-128">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="41697-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="41697-129"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="41697-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="41697-130">Der *ConfigurationName* -Parameter oder der *ConfigurationPath* -Parameter ist ungültig, oder der *virtualmachine* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="41697-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="41697-131"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="41697-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="41697-132">Das System kann den vom *ConfigurationPath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="41697-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="41697-133"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="41697-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="41697-134">Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="41697-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="41697-135"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="41697-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="41697-136">Der *ConfigurationPath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="41697-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="41697-137">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41697-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="41697-138"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="41697-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="41697-139">Der von den Parametern *ConfigurationName* und *ConfigurationPath* angegebene Pfad führt zu einem Pfad, der zu lang ist.</span><span class="sxs-lookup"><span data-stu-id="41697-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="41697-140">Die Gesamtlänge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="41697-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="41697-141"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="41697-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="41697-142">An diesem Speicherort ist bereits eine Konfigurationsdatei mit diesem Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41697-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="41697-143"><dt>**VM \_ E \_ config \_ No \_ Name**</dt> <dt>0xa0040400</dt></span><span class="sxs-lookup"><span data-stu-id="41697-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="41697-144">Der *ConfigurationName* -Parameter ist leer.</span><span class="sxs-lookup"><span data-stu-id="41697-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="41697-145"><dt>**VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang**</dt> <dt>0xa0040401</dt></span><span class="sxs-lookup"><span data-stu-id="41697-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="41697-146">Der *ConfigurationName* -Parameter überschreitet 80 Zeichen lang.</span><span class="sxs-lookup"><span data-stu-id="41697-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="41697-147"><dt>**VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char**</dt> <dt>0xa0040402</dt></span><span class="sxs-lookup"><span data-stu-id="41697-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="41697-148">Der *ConfigurationName* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen \* : "?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="41697-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="41697-149"><dt>**VM \_ E \_ config \_ Duplicate \_ Name**</dt> <dt>0xa0040403</dt></span><span class="sxs-lookup"><span data-stu-id="41697-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="41697-150">Es ist bereits ein virtueller Computer mit diesem Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41697-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="41697-151"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="41697-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="41697-152">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="41697-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="41697-153"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="41697-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="41697-154">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="41697-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="41697-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41697-155">Remarks</span></span>

<span data-ttu-id="41697-156">Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" beziehen sich auf denselben virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="41697-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="41697-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41697-157">Requirements</span></span>



| <span data-ttu-id="41697-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41697-158">Requirement</span></span> | <span data-ttu-id="41697-159">Wert</span><span class="sxs-lookup"><span data-stu-id="41697-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="41697-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41697-160">Minimum supported client</span></span><br/> | <span data-ttu-id="41697-161">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41697-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41697-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41697-162">Minimum supported server</span></span><br/> | <span data-ttu-id="41697-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41697-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="41697-164">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="41697-164">End of client support</span></span><br/>    | <span data-ttu-id="41697-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="41697-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="41697-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="41697-166">Product</span></span><br/>                  | <span data-ttu-id="41697-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="41697-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="41697-168">Header</span><span class="sxs-lookup"><span data-stu-id="41697-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="41697-169"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="41697-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="41697-170">IID</span><span class="sxs-lookup"><span data-stu-id="41697-170">IID</span></span><br/>                      | <span data-ttu-id="41697-171">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="41697-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="41697-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41697-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41697-173">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="41697-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

