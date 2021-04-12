---
title: Ivmvirtualmachine-Methode ("vpccominterfaces. h")
description: Legt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer fest.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Methode "stactivationvalue" Virtual PC
- Ctactivationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Methode "-Methode"
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478333"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="9a4e2-106">Ivmvirtualmachine:: abtactivationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="9a4e2-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="9a4e2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9a4e2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9a4e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9a4e2-109">Legt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4e2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a4e2-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="9a4e2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a4e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a4e2-112">*activationkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a4e2-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a4e2-113">Der Schlüssel, der verwendet wird, um den Aktivierungs Wert zu identifizieren, wie er in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="9a4e2-114">*activationvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a4e2-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a4e2-115">Der Aktivierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-115">The activation value.</span></span> <span data-ttu-id="9a4e2-116">Bei diesem Wert kann es sich um einen der folgenden **Variant** -Typen handeln: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="9a4e2-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a4e2-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a4e2-117">Return value</span></span>

<span data-ttu-id="9a4e2-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="9a4e2-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9a4e2-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="9a4e2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a4e2-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a4e2-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="9a4e2-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="9a4e2-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="9a4e2-124">Der *activationkey* -Parameter ist **null** oder leer, oder der *activationvalue* -Parameter ist kein gültiger VARIANT-Typ.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="9a4e2-125"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="9a4e2-126">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="9a4e2-127"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="9a4e2-128">Die Konfiguration hat keine gültige Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="9a4e2-129"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="9a4e2-130">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="9a4e2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a4e2-131">Remarks</span></span>

<span data-ttu-id="9a4e2-132">Diese Methode bietet Zugriff auf niedriger Ebene auf jeden Aktivierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="9a4e2-133">Sie kann verwendet werden, um Aktivierungs Werte für Kunden definierte Schlüssel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="9a4e2-134">Gehen Sie vorsichtig vor, wenn Sie diese Methode verwenden, um System Aktivierungs Werte festzulegen, da für den Aktivierungs Wert keine Fehlerüberprüfung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="9a4e2-135">Außerdem können einige Aktivierungs Werte nicht geändert werden, während der virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="9a4e2-136">Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte erstellt, die zu dem Satz von Aktivierungs Werten wird.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="9a4e2-137">Aktivierungs Werte werden so lange beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="9a4e2-138">Beachten Sie, dass Windows Virtual PC die Konfiguration möglicherweise nur zum Speichern von Werten für bestimmte Schlüssel verwendet, d. h., der Aktivierungs Wert darf nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="9a4e2-139">Die Sitzung für virtuelle Computer muss ausgeführt werden, bevor Aktivierungs Werte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="9a4e2-140">Aktivierungsschlüssel werden auf hierarchische Weise wie die Registrierungsschlüssel in Windows gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="9a4e2-141">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="9a4e2-142">So legen Sie z. b. den Wert des Schlüssels "Default Action" fest, der \_ sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="9a4e2-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="9a4e2-143">Die Pfad Zeichenfolge von *activationkey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="9a4e2-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="9a4e2-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a4e2-144">Requirements</span></span>



| <span data-ttu-id="9a4e2-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a4e2-145">Requirement</span></span> | <span data-ttu-id="9a4e2-146">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4e2-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4e2-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a4e2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4e2-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a4e2-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a4e2-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a4e2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4e2-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a4e2-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9a4e2-151">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9a4e2-151">End of client support</span></span><br/>    | <span data-ttu-id="9a4e2-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a4e2-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9a4e2-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="9a4e2-153">Product</span></span><br/>                  | <span data-ttu-id="9a4e2-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9a4e2-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9a4e2-155">Header</span><span class="sxs-lookup"><span data-stu-id="9a4e2-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a4e2-156"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a4e2-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9a4e2-157">IID</span><span class="sxs-lookup"><span data-stu-id="9a4e2-157">IID</span></span><br/>                      | <span data-ttu-id="9a4e2-158">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="9a4e2-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9a4e2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a4e2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4e2-160">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="9a4e2-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

