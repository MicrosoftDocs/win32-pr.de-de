---
title: Ivmvirtualmachine setconfigurationvalue-Methode (vpccominterfaces. h)
description: Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer (VM) fest.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Setconfigurationvalue-Methode Virtual PC
- Setconfigurationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, setconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344489"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="4f47a-106">Ivmvirtualmachine:: setconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="4f47a-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="4f47a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f47a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4f47a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4f47a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4f47a-109">Legt den Wert der angegebenen Konfigurationseinstellung für diesen virtuellen Computer (VM) fest.</span><span class="sxs-lookup"><span data-stu-id="4f47a-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f47a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f47a-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="4f47a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f47a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f47a-112">*ConfigurationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f47a-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f47a-113">Der Schlüssel, der zum Identifizieren des Konfigurations Werts verwendet wird, der in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4f47a-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f47a-114">Änderungen sollten \* nur mit der **setconfigurationvalue** -Methode an ". vmc" vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4f47a-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="4f47a-115">Das ändern \* von ". vmc" mit einer anderen Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f47a-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="4f47a-116">*configurationvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f47a-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f47a-117">Der Konfigurationswert.</span><span class="sxs-lookup"><span data-stu-id="4f47a-117">The configuration value.</span></span> <span data-ttu-id="4f47a-118">Dieser Wert ist einer der folgenden **Variant** -Typen: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="4f47a-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f47a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f47a-119">Return value</span></span>

<span data-ttu-id="4f47a-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4f47a-120">This method can return one of these values.</span></span>



| <span data-ttu-id="4f47a-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4f47a-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="4f47a-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f47a-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f47a-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4f47a-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f47a-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="4f47a-125"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="4f47a-126">Der *ConfigurationKey* -Parameter ist **null** oder leer, oder der *configurationvalue* -Parameter ist kein gültiger VARIANT-Typ.</span><span class="sxs-lookup"><span data-stu-id="4f47a-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="4f47a-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4f47a-128">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="4f47a-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="4f47a-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4f47a-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4f47a-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="4f47a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f47a-131">Remarks</span></span>

<span data-ttu-id="4f47a-132">Die folgenden Werte werden für den *ConfigurationKey* -Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f47a-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="4f47a-133">*ConfigurationKey* -Wert</span><span class="sxs-lookup"><span data-stu-id="4f47a-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="4f47a-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f47a-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="4f47a-135">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4f47a-135">Data type</span></span>            | <span data-ttu-id="4f47a-136">Standardwert</span><span class="sxs-lookup"><span data-stu-id="4f47a-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="4f47a-137">"Hardware/BIOS/Zeit \_ Synchronisierung \_ beim \_ Start"</span><span class="sxs-lookup"><span data-stu-id="4f47a-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="4f47a-138">"true", wenn die VM-CMOS-Uhr beim Start mit der hostuhr synchronisiert werden soll. andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="4f47a-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="4f47a-139">booleschen</span><span class="sxs-lookup"><span data-stu-id="4f47a-139">"boolean"</span></span><br/> | <span data-ttu-id="4f47a-140">"true"</span><span class="sxs-lookup"><span data-stu-id="4f47a-140">"true"</span></span><br/> |
| <span data-ttu-id="4f47a-141">"Integration/Microsoft/ \_ hostzeit \_ Synchronisierung/aktiviert" "</span><span class="sxs-lookup"><span data-stu-id="4f47a-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="4f47a-142">"true", wenn die Host Zeitsynchronisierung in den Integrations Komponenten aktiviert ist. andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="4f47a-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="4f47a-143">booleschen</span><span class="sxs-lookup"><span data-stu-id="4f47a-143">"boolean"</span></span><br/> | <span data-ttu-id="4f47a-144">"true"</span><span class="sxs-lookup"><span data-stu-id="4f47a-144">"true"</span></span><br/> |
| <span data-ttu-id="4f47a-145">"UI \_ -Optionen/Automatische \_ App- \_ Veröffentlichung"</span><span class="sxs-lookup"><span data-stu-id="4f47a-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="4f47a-146">"true", wenn die automatische Veröffentlichung von Anwendungen in den Integrations Komponenten aktiviert ist. andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="4f47a-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="4f47a-147">Dies wird auch als virtuelle Anwendungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4f47a-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="4f47a-148">booleschen</span><span class="sxs-lookup"><span data-stu-id="4f47a-148">"boolean"</span></span><br/> | <span data-ttu-id="4f47a-149">"true"</span><span class="sxs-lookup"><span data-stu-id="4f47a-149">"true"</span></span><br/> |
| <span data-ttu-id="4f47a-150">"Benutzeroberflächen \_ Optionen/-Sekunden \_ zum \_ Speichern"</span><span class="sxs-lookup"><span data-stu-id="4f47a-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="4f47a-151">Anzahl von Sekunden, die gewartet werden soll, bevor die VM gespeichert wird, nachdem alle Anwendungen geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="4f47a-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="4f47a-152">Werte unter 20 und mehr als 4.294.968 haben jedoch eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4f47a-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="4f47a-153">Weitere Informationen finden Sie in der folgenden Liste:</span><span class="sxs-lookup"><span data-stu-id="4f47a-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="4f47a-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="4f47a-155">Speichern Sie die VM nie.</span><span class="sxs-lookup"><span data-stu-id="4f47a-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="4f47a-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="4f47a-157">Warten Sie 20 Sekunden, bevor Sie den virtuellen Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="4f47a-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="4f47a-158"><dt><span id="214_294_967"></span>21 4.294.967</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="4f47a-159">Warten Sie die angegebene Anzahl von Sekunden, bevor Sie den virtuellen Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="4f47a-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="4f47a-160"><dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="4f47a-161">Warten Sie 4.294.968 Sekunden, bevor Sie den virtuellen Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="4f47a-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="4f47a-162">Zah</span><span class="sxs-lookup"><span data-stu-id="4f47a-162">"integer"</span></span><br/> | <span data-ttu-id="4f47a-163">300</span><span class="sxs-lookup"><span data-stu-id="4f47a-163">300</span></span><br/>    |



 

<span data-ttu-id="4f47a-164">Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert.</span><span class="sxs-lookup"><span data-stu-id="4f47a-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="4f47a-165">Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4f47a-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="4f47a-166">Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemkonfigurations Werte festzulegen, da für den Konfigurations Wert keine Fehlerüberprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f47a-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="4f47a-167">Außerdem können einige Konfigurationswerte nicht geändert werden, während der virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f47a-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="4f47a-168">Konfigurationsschlüssel befinden sich in der VMC-Datei der virtuellen Maschine \* im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="4f47a-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="4f47a-169">Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows.</span><span class="sxs-lookup"><span data-stu-id="4f47a-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="4f47a-170">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="4f47a-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="4f47a-171">So legen Sie beispielsweise den Wert für den Schlüssel "RAM size" fest, der \_ sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="4f47a-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="4f47a-172">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="4f47a-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="4f47a-173">Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der *ConfigurationKey* -Pfad Zeichenfolge unmittelbar nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".</span><span class="sxs-lookup"><span data-stu-id="4f47a-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="4f47a-174">So legen Sie beispielsweise den Wert des "Golf"-Schlüssels fest, der sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="4f47a-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="4f47a-175">Die Pfad Zeichenfolge für *ConfigurationKey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="4f47a-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="4f47a-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f47a-176">Requirements</span></span>



| <span data-ttu-id="4f47a-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f47a-177">Requirement</span></span> | <span data-ttu-id="4f47a-178">Wert</span><span class="sxs-lookup"><span data-stu-id="4f47a-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f47a-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f47a-179">Minimum supported client</span></span><br/> | <span data-ttu-id="4f47a-180">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f47a-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f47a-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f47a-181">Minimum supported server</span></span><br/> | <span data-ttu-id="4f47a-182">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4f47a-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4f47a-183">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4f47a-183">End of client support</span></span><br/>    | <span data-ttu-id="4f47a-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f47a-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4f47a-185">Produkt</span><span class="sxs-lookup"><span data-stu-id="4f47a-185">Product</span></span><br/>                  | <span data-ttu-id="4f47a-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4f47a-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4f47a-187">Header</span><span class="sxs-lookup"><span data-stu-id="4f47a-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f47a-188"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f47a-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4f47a-189">IID</span><span class="sxs-lookup"><span data-stu-id="4f47a-189">IID</span></span><br/>                      | <span data-ttu-id="4f47a-190">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="4f47a-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4f47a-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f47a-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f47a-192">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="4f47a-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="4f47a-193">**Ivmvirtualpc:: setconfigurationvalue**</span><span class="sxs-lookup"><span data-stu-id="4f47a-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

