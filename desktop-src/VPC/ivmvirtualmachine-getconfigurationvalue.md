---
title: Ivmvirtualmachine getconfigurationvalue-Methode (vpccominterfaces. h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Getconfigurationvalue-Methode Virtual PC
- Getconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, getconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391982"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="bb12e-106">Ivmvirtualmachine:: getconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="bb12e-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="bb12e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb12e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb12e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb12e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb12e-109">Ruft den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="bb12e-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb12e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb12e-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="bb12e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb12e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb12e-112">*ConfigurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb12e-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb12e-113">Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bb12e-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="bb12e-114">*configurationvalue* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bb12e-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bb12e-115">Der Konfigurationswert.</span><span class="sxs-lookup"><span data-stu-id="bb12e-115">The configuration value.</span></span> <span data-ttu-id="bb12e-116">Bei diesem Wert kann es sich um einen der folgenden **Variant** -Typen handeln: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="bb12e-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb12e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb12e-117">Return value</span></span>

<span data-ttu-id="bb12e-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb12e-118">This method can return one of these values.</span></span>



| <span data-ttu-id="bb12e-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bb12e-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="bb12e-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb12e-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb12e-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="bb12e-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb12e-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="bb12e-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="bb12e-124">Der *ConfigurationKey* -Parameter ist **null** oder leer.</span><span class="sxs-lookup"><span data-stu-id="bb12e-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="bb12e-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="bb12e-126">Der *configurationvalue* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="bb12e-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="bb12e-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="bb12e-128">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="bb12e-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="bb12e-129"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="bb12e-130">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="bb12e-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="bb12e-131"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="bb12e-132">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bb12e-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="bb12e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb12e-133">Remarks</span></span>

<span data-ttu-id="bb12e-134">Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert.</span><span class="sxs-lookup"><span data-stu-id="bb12e-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="bb12e-135">Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel zu lesen.</span><span class="sxs-lookup"><span data-stu-id="bb12e-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="bb12e-136">Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="bb12e-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="bb12e-137">Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows.</span><span class="sxs-lookup"><span data-stu-id="bb12e-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="bb12e-138">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="bb12e-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="bb12e-139">Um z. b. den Wert des Schlüssels "RAM \_ size" in der folgenden Schlüsselstruktur zu lesen:</span><span class="sxs-lookup"><span data-stu-id="bb12e-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="bb12e-140">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="bb12e-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="bb12e-141">Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der *ConfigurationKey* -Pfad Zeichenfolge unmittelbar nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".</span><span class="sxs-lookup"><span data-stu-id="bb12e-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="bb12e-142">Um z. b. den Wert des "absoluten" Schlüssels in der folgenden Schlüsselstruktur zu lesen:</span><span class="sxs-lookup"><span data-stu-id="bb12e-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="bb12e-143">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="bb12e-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="bb12e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb12e-144">Requirements</span></span>



| <span data-ttu-id="bb12e-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb12e-145">Requirement</span></span> | <span data-ttu-id="bb12e-146">Wert</span><span class="sxs-lookup"><span data-stu-id="bb12e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb12e-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb12e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bb12e-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb12e-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb12e-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb12e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bb12e-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bb12e-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb12e-151">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bb12e-151">End of client support</span></span><br/>    | <span data-ttu-id="bb12e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb12e-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb12e-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="bb12e-153">Product</span></span><br/>                  | <span data-ttu-id="bb12e-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb12e-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb12e-155">Header</span><span class="sxs-lookup"><span data-stu-id="bb12e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb12e-156"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb12e-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb12e-157">IID</span><span class="sxs-lookup"><span data-stu-id="bb12e-157">IID</span></span><br/>                      | <span data-ttu-id="bb12e-158">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="bb12e-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bb12e-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb12e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb12e-160">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="bb12e-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

