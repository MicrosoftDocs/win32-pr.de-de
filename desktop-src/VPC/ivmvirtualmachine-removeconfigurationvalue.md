---
title: Ivmvirtualmachine removeconfigurationvalue-Methode (vpccominterfaces. h)
description: Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Removeconfigurationvalue-Methode Virtual PC
- Removeconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477985"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="ad257-106">Ivmvirtualmachine:: removeconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="ad257-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="ad257-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad257-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ad257-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad257-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ad257-109">Entfernt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ad257-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad257-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad257-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="ad257-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad257-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad257-112">*ConfigurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad257-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad257-113">Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ad257-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad257-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad257-114">Return value</span></span>

<span data-ttu-id="ad257-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ad257-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ad257-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ad257-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="ad257-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad257-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ad257-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="ad257-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad257-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="ad257-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="ad257-121">Der-Parameter ist **null** oder leer.</span><span class="sxs-lookup"><span data-stu-id="ad257-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="ad257-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="ad257-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ad257-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="ad257-124"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="ad257-125">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ad257-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="ad257-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="ad257-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ad257-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="ad257-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad257-128">Remarks</span></span>

<span data-ttu-id="ad257-129">Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert.</span><span class="sxs-lookup"><span data-stu-id="ad257-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="ad257-130">Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ad257-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="ad257-131">Gehen Sie vorsichtig vor, wenn Sie mit dieser Methode Systemkonfigurationswerte entfernen, da einige Werte nicht geändert werden können, während die virtuelle Maschine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad257-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="ad257-132">Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="ad257-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="ad257-133">Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows.</span><span class="sxs-lookup"><span data-stu-id="ad257-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="ad257-134">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="ad257-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="ad257-135">Um beispielsweise den Wert des Schlüssels "RAM size" zu entfernen, der \_ sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="ad257-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="ad257-136">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="ad257-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="ad257-137">Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der *ConfigurationKey* -Pfad Zeichenfolge unmittelbar nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".</span><span class="sxs-lookup"><span data-stu-id="ad257-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="ad257-138">Um z. b. den Wert des "absoluten" Schlüssels zu entfernen, der sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="ad257-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="ad257-139">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="ad257-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="ad257-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad257-140">Requirements</span></span>



| <span data-ttu-id="ad257-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad257-141">Requirement</span></span> | <span data-ttu-id="ad257-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ad257-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad257-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad257-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ad257-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad257-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad257-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad257-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ad257-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad257-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ad257-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ad257-147">End of client support</span></span><br/>    | <span data-ttu-id="ad257-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad257-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad257-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="ad257-149">Product</span></span><br/>                  | <span data-ttu-id="ad257-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ad257-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ad257-151">Header</span><span class="sxs-lookup"><span data-stu-id="ad257-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad257-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad257-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ad257-153">IID</span><span class="sxs-lookup"><span data-stu-id="ad257-153">IID</span></span><br/>                      | <span data-ttu-id="ad257-154">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="ad257-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ad257-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad257-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad257-156">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="ad257-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

