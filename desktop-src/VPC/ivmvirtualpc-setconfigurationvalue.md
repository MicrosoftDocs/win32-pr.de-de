---
title: Ivmvirtualpc setconfigurationvalue-Methode (vpccominterfaces. h)
description: Legt den Wert der angegebenen Konfigurationseinstellung fest.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Setconfigurationvalue-Methode Virtual PC
- Setconfigurationvalue-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, setconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518467"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="65092-106">Ivmvirtualpc:: setconfigurationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="65092-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="65092-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65092-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="65092-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="65092-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="65092-109">Legt den Wert der angegebenen Konfigurationseinstellung fest.</span><span class="sxs-lookup"><span data-stu-id="65092-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="65092-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="65092-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="65092-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="65092-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65092-112">*preferecekey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65092-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65092-113">Der Schlüssel, der verwendet wird, um die Einstellung zu identifizieren, wie Sie in der Konfigurationsdatei pro Benutzer (Options.xml in "% LocalAppData% \\ Microsoft \\ Windows Virtual PC") gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="65092-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65092-114">Es sollten Änderungen vorgenommen werden, die nur mit der **setconfigurationvalue** -Methode Options.xml werden.</span><span class="sxs-lookup"><span data-stu-id="65092-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="65092-115">Das Ändern von Options.xml mit einer anderen Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65092-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="65092-116">*preferumcevalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65092-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65092-117">Der bevorzugte Wert.</span><span class="sxs-lookup"><span data-stu-id="65092-117">The preference value.</span></span> <span data-ttu-id="65092-118">Dieser Wert kann einer der folgenden **Variant** -Typen sein: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="65092-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65092-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65092-119">Return value</span></span>

<span data-ttu-id="65092-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="65092-120">This method can return one of these values.</span></span>



| <span data-ttu-id="65092-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="65092-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="65092-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65092-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65092-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="65092-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="65092-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="65092-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="65092-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="65092-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="65092-126">Der *preferecekey* -Parameter oder der *preferendcevalue* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="65092-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="65092-127"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="65092-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="65092-128">Der *preferencekey* -Parameter ist ungültig oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="65092-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="65092-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="65092-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="65092-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="65092-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="65092-131"><dt>**E \_ AccessDenied**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="65092-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="65092-132">Der aktuelle Benutzer verfügt nicht über ausreichenden Zugriff auf die Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="65092-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="65092-133"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="65092-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="65092-134">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="65092-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65092-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65092-135">Remarks</span></span>

<span data-ttu-id="65092-136">Die folgenden Werte werden für den *preferecekey* -Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="65092-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="65092-137">*preferecekey* -Wert</span><span class="sxs-lookup"><span data-stu-id="65092-137">*preferenceKey* value</span></span>      | <span data-ttu-id="65092-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65092-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="65092-139">Datentyp</span><span class="sxs-lookup"><span data-stu-id="65092-139">Data type</span></span>            | <span data-ttu-id="65092-140">Standardwert</span><span class="sxs-lookup"><span data-stu-id="65092-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="65092-141">"Leerlauf \_ Timeout"</span><span class="sxs-lookup"><span data-stu-id="65092-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="65092-142">Anzahl der Sekunden, die vpc.exe warten soll, bis der Vorgang beendet ist, wenn die [Windows Virtual PC-Schnittstellen](virtual-pc-interfaces.md)keine aktiven VMS oder Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="65092-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="65092-143">Zah</span><span class="sxs-lookup"><span data-stu-id="65092-143">"integer"</span></span><br/> | <span data-ttu-id="65092-144">„30“</span><span class="sxs-lookup"><span data-stu-id="65092-144">"30"</span></span><br/> |



 

<span data-ttu-id="65092-145">Diese Methode bietet Zugriff auf niedriger Ebene auf einen beliebigen Konfigurations Wert.</span><span class="sxs-lookup"><span data-stu-id="65092-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="65092-146">Sie kann verwendet werden, um Konfigurationswerte für Kunden definierte Schlüssel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="65092-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="65092-147">Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um Systemkonfigurations Werte festzulegen, da für den Konfigurations Wert keine Fehlerüberprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65092-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="65092-148">Außerdem können einige Konfigurationswerte nicht geändert werden, während ein virtueller Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65092-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="65092-149">Konfigurationsschlüssel befinden sich im XML-Format in der Datei "Options.xml" der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="65092-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="65092-150">Die Schlüssel werden auf hierarchische Weise gespeichert, ähnlich wie die Registrierungsschlüssel in Windows.</span><span class="sxs-lookup"><span data-stu-id="65092-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="65092-151">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="65092-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="65092-152">So legen Sie beispielsweise den Wert für den Schlüssel "Leerlauf Timeout" fest, der \_ sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="65092-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="65092-153">Die Pfad *Zeichenfolge für den preferencekey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="65092-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="65092-154">Wenn einer der Schlüssel in der gewünschten Struktur über einen "ID"-Attribut Wert verfügt, werden das Attribut und sein Wert in der Pfad *Zeichenfolge "preferencekey* " direkt nach dem zugehörigen Konfigurationsschlüssel in folgendem Format in Klammern eingebettet: " \[ @id ="*ID- \_ Wert*" \] ".</span><span class="sxs-lookup"><span data-stu-id="65092-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="65092-155">So legen Sie beispielsweise den Wert des "Golf"-Schlüssels fest, der sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="65092-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="65092-156">Die Pfad *Zeichenfolge für den preferencekey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="65092-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="65092-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65092-157">Requirements</span></span>



| <span data-ttu-id="65092-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65092-158">Requirement</span></span> | <span data-ttu-id="65092-159">Wert</span><span class="sxs-lookup"><span data-stu-id="65092-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65092-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65092-160">Minimum supported client</span></span><br/> | <span data-ttu-id="65092-161">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65092-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65092-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65092-162">Minimum supported server</span></span><br/> | <span data-ttu-id="65092-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="65092-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="65092-164">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="65092-164">End of client support</span></span><br/>    | <span data-ttu-id="65092-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65092-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="65092-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="65092-166">Product</span></span><br/>                  | <span data-ttu-id="65092-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="65092-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="65092-168">Header</span><span class="sxs-lookup"><span data-stu-id="65092-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="65092-169"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="65092-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="65092-170">IID</span><span class="sxs-lookup"><span data-stu-id="65092-170">IID</span></span><br/>                      | <span data-ttu-id="65092-171">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="65092-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="65092-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65092-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65092-173">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="65092-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="65092-174">**Ivmvirtualmachine:: setconfigurationvalue**</span><span class="sxs-lookup"><span data-stu-id="65092-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

