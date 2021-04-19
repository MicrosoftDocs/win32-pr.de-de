---
title: Ivmvirtualpc registervirtualmachine-Methode (vpccominterfaces. h)
description: Registriert eine vorhandene VM-Konfiguration und ruft das Objekt der virtuellen Maschine ab.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Registervirtualmachine-Methode Virtual PC
- Registervirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, registervirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342471"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="e22c7-106">Ivmvirtualpc:: registervirtualmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="e22c7-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="e22c7-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e22c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e22c7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e22c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e22c7-109">Registriert eine vorhandene VM-Konfiguration und ruft das Objekt der virtuellen Maschine ab.</span><span class="sxs-lookup"><span data-stu-id="e22c7-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22c7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e22c7-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="e22c7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e22c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22c7-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e22c7-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e22c7-113">Der Name des zu registrierenden virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e22c7-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="e22c7-114">Der Name darf nicht länger als 80 Zeichen sein, und die kombinierte Länge des Namens und des Pfads darf **maximal \_ zulässige (** 260) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e22c7-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="e22c7-115">Der angegebene Name kann die VMC-Erweiterung enthalten.</span><span class="sxs-lookup"><span data-stu-id="e22c7-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="e22c7-116">Wenn dieser Parameter **null** oder eine leere Zeichenfolge ist, muss der *ConfigurationPath* -Parameter den vollständigen Pfad zur Konfigurationsdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="e22c7-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="e22c7-117">*ConfigurationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e22c7-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e22c7-118">Der Pfad zu dem Ordner, der die vorhandene Konfigurationsdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="e22c7-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="e22c7-119">Wenn der *ConfigurationName* -Parameter **null** oder eine leere Zeichenfolge ist, muss der vollständige Pfad zur vorhandenen Konfigurationsdatei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e22c7-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="e22c7-120">*virtualmachine* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e22c7-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e22c7-121">Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="e22c7-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22c7-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e22c7-122">Return value</span></span>

<span data-ttu-id="e22c7-123">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e22c7-123">This method can return one of these values.</span></span>



| <span data-ttu-id="e22c7-124">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e22c7-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="e22c7-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e22c7-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e22c7-126"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="e22c7-127">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e22c7-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="e22c7-128"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="e22c7-129">Der *ConfigurationName* -Parameter oder der *ConfigurationPath* -Parameter ist ungültig, oder *virtualmachine* ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e22c7-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="e22c7-130"><dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="e22c7-131">Das System kann den in den Parametern *ConfigurationName* und *ConfigurationPath* angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="e22c7-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="e22c7-132"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="e22c7-133">Das System kann die durch den *ConfigurationName* -Parameter und den *ConfigurationPath* -Parameter angegebene Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="e22c7-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="e22c7-134"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="e22c7-135">Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines von " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="e22c7-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="e22c7-136"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="e22c7-137">Der *ConfigurationPath* -Parameter des Parameters gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="e22c7-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="e22c7-138">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e22c7-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="e22c7-139"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="e22c7-140">Der von den Parametern *ConfigurationName* und *ConfigurationPath* angegebene Pfad führt zu einem Pfad, der zu lang ist.</span><span class="sxs-lookup"><span data-stu-id="e22c7-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="e22c7-141">Die kombinierte Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="e22c7-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="e22c7-142"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="e22c7-143">An diesem Speicherort ist bereits eine Konfigurationsdatei mit diesem Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e22c7-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="e22c7-144"><dt>**VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang**</dt> <dt>0xa0040401</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="e22c7-145">Der *ConfigurationName* -Parameter überschreitet 80 Zeichen lang.</span><span class="sxs-lookup"><span data-stu-id="e22c7-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="e22c7-146"><dt>**VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char**</dt> <dt>0xa0040402</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="e22c7-147">Der *ConfigurationName* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen \* : "?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="e22c7-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="e22c7-148"><dt>**VM \_ E \_ config \_ Duplicate \_ Name**</dt> <dt>0xa0040403</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="e22c7-149">Es ist bereits ein virtueller Computer mit diesem Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e22c7-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="e22c7-150"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="e22c7-151">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="e22c7-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="e22c7-152"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="e22c7-153">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e22c7-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="e22c7-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e22c7-154">Remarks</span></span>

<span data-ttu-id="e22c7-155">Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" beziehen sich auf denselben virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e22c7-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="e22c7-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e22c7-156">Requirements</span></span>



| <span data-ttu-id="e22c7-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e22c7-157">Requirement</span></span> | <span data-ttu-id="e22c7-158">Wert</span><span class="sxs-lookup"><span data-stu-id="e22c7-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22c7-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e22c7-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e22c7-160">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e22c7-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e22c7-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e22c7-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e22c7-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e22c7-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e22c7-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e22c7-163">End of client support</span></span><br/>    | <span data-ttu-id="e22c7-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e22c7-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e22c7-165">Produkt</span><span class="sxs-lookup"><span data-stu-id="e22c7-165">Product</span></span><br/>                  | <span data-ttu-id="e22c7-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e22c7-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e22c7-167">Header</span><span class="sxs-lookup"><span data-stu-id="e22c7-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="e22c7-168"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22c7-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e22c7-169">IID</span><span class="sxs-lookup"><span data-stu-id="e22c7-169">IID</span></span><br/>                      | <span data-ttu-id="e22c7-170">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="e22c7-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e22c7-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e22c7-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22c7-172">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="e22c7-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

