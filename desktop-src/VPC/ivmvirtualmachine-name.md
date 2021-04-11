---
title: Ivmvirtualmachine-Name-Eigenschaft (vpccominterfaces. h)
description: Der Name der Konfiguration der virtuellen Maschine.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104102"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="ff9e5-106">Ivmvirtualmachine:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ff9e5-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="ff9e5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff9e5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff9e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff9e5-109">Ruft den Namen der Konfiguration der virtuellen Maschine ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="ff9e5-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9e5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff9e5-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="ff9e5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ff9e5-112">Property value</span></span>

<span data-ttu-id="ff9e5-113">Gibt den Namen der Konfiguration der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="ff9e5-114">Die Länge des Namens darf nicht mehr als 80 Zeichen betragen, und die Gesamtlänge des voll qualifizierten Pfads, der die Konfigurationsdatei für den virtuellen Computer enthält, darf nicht größer als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff9e5-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ff9e5-115">Error codes</span></span>



| <span data-ttu-id="ff9e5-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ff9e5-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="ff9e5-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff9e5-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff9e5-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="ff9e5-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ff9e5-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="ff9e5-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ff9e5-122"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="ff9e5-123">Der-Parameter ist ungültig oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ff9e5-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="ff9e5-125">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ff9e5-126"><dt>VM \_ E \_ Pref- \_ VM \_ aktiv</dt> <dt>0xa0040302</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="ff9e5-127">Der virtuelle Computer wird ausgeführt oder gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="ff9e5-128"><dt>VM \_ E \_ config \_ No \_ Name</dt> <dt>0xa0040400</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="ff9e5-129">Der *virtualmachinename* -Parameter ist leer.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ff9e5-130"><dt>VM \_ E- \_ Konfigurations \_ Name \_ zu \_ lang</dt> <dt>0xa00400401</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="ff9e5-131">Der-Parameter enthält zu viele Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="ff9e5-132"><dt>VM \_ E- \_ Konfigurations \_ Name ist \_ ungültig \_ char</dt> <dt>0xa0040402</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="ff9e5-133">Der-Parameter enthält eines der folgenden ungültigen Zeichen \* : "?: <>/ \| \\ " ".</span><span class="sxs-lookup"><span data-stu-id="ff9e5-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="ff9e5-134"><dt>VM \_ E \_ config \_ Duplicate \_ Name</dt> <dt>0xa0040403</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="ff9e5-135">Der angegebene Name ist bereits als Name eines anderen virtuellen Computers vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="ff9e5-136"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="ff9e5-137">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="ff9e5-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff9e5-138">Remarks</span></span>

<span data-ttu-id="ff9e5-139">Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" verweisen auf denselben virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="ff9e5-140">Dies ist die Standard Eigenschaft für [**ivmvirtualmachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="ff9e5-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="ff9e5-141">Wenn VPC.exe ausgeführt wird und die VM gespeichert wird, wird das Festlegen der **Name** -Eigenschaft nicht erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="ff9e5-142">Wenn VPC.exe nicht ausgeführt wird und die VM gespeichert wird, ist das Festlegen der **Name** -Eigenschaft erfolgreich, wenn VPC.exe das nächste Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9e5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff9e5-143">Requirements</span></span>



| <span data-ttu-id="ff9e5-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff9e5-144">Requirement</span></span> | <span data-ttu-id="ff9e5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ff9e5-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9e5-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff9e5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ff9e5-147">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff9e5-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff9e5-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff9e5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ff9e5-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff9e5-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff9e5-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ff9e5-150">End of client support</span></span><br/>    | <span data-ttu-id="ff9e5-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff9e5-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff9e5-152">Produkt</span><span class="sxs-lookup"><span data-stu-id="ff9e5-152">Product</span></span><br/>                  | <span data-ttu-id="ff9e5-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff9e5-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff9e5-154">Header</span><span class="sxs-lookup"><span data-stu-id="ff9e5-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff9e5-155"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff9e5-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff9e5-156">IID</span><span class="sxs-lookup"><span data-stu-id="ff9e5-156">IID</span></span><br/>                      | <span data-ttu-id="ff9e5-157">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ff9e5-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff9e5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9e5-159">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="ff9e5-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

