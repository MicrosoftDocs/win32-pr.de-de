---
title: Ivmvirtualmachine getactivationvalue-Methode (vpccominterfaces. h)
description: Ruft den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer ab.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Getactivationvalue-Methode Virtual PC
- Getactivationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, getactivationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340317"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="2cdbc-106">Ivmvirtualmachine:: getactivationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="2cdbc-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="2cdbc-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2cdbc-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2cdbc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2cdbc-109">Ruft den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cdbc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cdbc-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="2cdbc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cdbc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cdbc-112">*activationkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cdbc-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdbc-113">Der Schlüssel, der verwendet wird, um den Aktivierungs Wert zu identifizieren, wie er in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="2cdbc-114">*activationvalue* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2cdbc-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdbc-115">Der Aktivierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-115">The activation value.</span></span> <span data-ttu-id="2cdbc-116">Bei diesem Wert kann es sich um einen der folgenden **Variant** -Typen handeln: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) oder **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="2cdbc-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cdbc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cdbc-117">Return value</span></span>

<span data-ttu-id="2cdbc-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-118">This method can return one of these values.</span></span>



| <span data-ttu-id="2cdbc-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2cdbc-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="2cdbc-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cdbc-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cdbc-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="2cdbc-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="2cdbc-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="2cdbc-124">Der *activationkey* -Parameter ist **null** oder leer.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="2cdbc-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="2cdbc-126">Der *activationvalue* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2cdbc-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="2cdbc-128">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="2cdbc-129"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="2cdbc-130">Die Einstellung wurde nicht gefunden, oder für diese Konfiguration ist keine gültige Aktivierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="2cdbc-131"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="2cdbc-132">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="2cdbc-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cdbc-133">Remarks</span></span>

<span data-ttu-id="2cdbc-134">Diese Methode bietet Zugriff auf niedriger Ebene auf jeden Aktivierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="2cdbc-135">Sie kann verwendet werden, um Aktivierungs Werte für Kunden definierte Schlüssel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="2cdbc-136">Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte erstellt, die zu dem Satz von Aktivierungs Werten wird.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="2cdbc-137">Aktivierungs Werte werden so lange beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="2cdbc-138">Beachten Sie, dass Windows Virtual PC die Konfiguration möglicherweise nur zum Speichern von Werten für bestimmte Schlüssel verwendet, d. h., der Aktivierungs Wert darf nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="2cdbc-139">Aktivierungsschlüssel werden auf hierarchische Weise wie die Registrierungsschlüssel in Windows gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="2cdbc-140">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="2cdbc-141">Um z. b. den Wert des Schlüssels "Default \_ action" in der folgenden Schlüsselstruktur zu lesen:</span><span class="sxs-lookup"><span data-stu-id="2cdbc-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="2cdbc-142">Die Pfad Zeichenfolge von *activationkey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="2cdbc-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="2cdbc-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cdbc-143">Requirements</span></span>



| <span data-ttu-id="2cdbc-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cdbc-144">Requirement</span></span> | <span data-ttu-id="2cdbc-145">Wert</span><span class="sxs-lookup"><span data-stu-id="2cdbc-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdbc-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cdbc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2cdbc-147">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cdbc-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cdbc-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cdbc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2cdbc-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2cdbc-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2cdbc-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2cdbc-150">End of client support</span></span><br/>    | <span data-ttu-id="2cdbc-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cdbc-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2cdbc-152">Produkt</span><span class="sxs-lookup"><span data-stu-id="2cdbc-152">Product</span></span><br/>                  | <span data-ttu-id="2cdbc-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2cdbc-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2cdbc-154">Header</span><span class="sxs-lookup"><span data-stu-id="2cdbc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cdbc-155"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cdbc-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2cdbc-156">IID</span><span class="sxs-lookup"><span data-stu-id="2cdbc-156">IID</span></span><br/>                      | <span data-ttu-id="2cdbc-157">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2cdbc-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cdbc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cdbc-159">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="2cdbc-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

