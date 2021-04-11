---
title: Ivmvirtualmachine removeactivationvalue-Methode (vpccominterfaces. h)
description: Entfernt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Removeactivationvalue-Methode Virtual PC
- Removeactivationvalue-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeactivationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040701"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="46f9c-106">Ivmvirtualmachine:: removeactivationvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="46f9c-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="46f9c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46f9c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46f9c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46f9c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46f9c-109">Entfernt den Wert der angegebenen Aktivierungs Einstellung für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="46f9c-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f9c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f9c-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="46f9c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f9c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f9c-112">*activationkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46f9c-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f9c-113">Der Schlüssel, der verwendet wird, um den Aktivierungs Wert zu identifizieren, wie er in der \* VMC-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="46f9c-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f9c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46f9c-114">Return value</span></span>

<span data-ttu-id="46f9c-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="46f9c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="46f9c-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="46f9c-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="46f9c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46f9c-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46f9c-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="46f9c-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="46f9c-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="46f9c-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="46f9c-121">Der-Parameter ist **null** oder leer.</span><span class="sxs-lookup"><span data-stu-id="46f9c-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="46f9c-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="46f9c-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="46f9c-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="46f9c-124"><dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="46f9c-125">Die Einstellung wurde nicht gefunden, oder für diese Konfiguration ist keine gültige Aktivierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="46f9c-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="46f9c-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="46f9c-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="46f9c-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="46f9c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46f9c-128">Remarks</span></span>

<span data-ttu-id="46f9c-129">Diese Methode bietet Zugriff auf niedriger Ebene auf jeden Aktivierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="46f9c-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="46f9c-130">Sie kann verwendet werden, um Aktivierungs Werte für Kunden definierte Schlüssel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="46f9c-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="46f9c-131">Gehen Sie vorsichtig vor, wenn Sie diese Methode zum Entfernen von System Aktivierungs Werten verwenden, da einige Werte nicht geändert werden können, während die virtuelle Maschine ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46f9c-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="46f9c-132">Wenn ein virtueller Computer gestartet wird, wird eine Kopie seiner Konfigurationswerte erstellt, die zu dem Satz von Aktivierungs Werten wird.</span><span class="sxs-lookup"><span data-stu-id="46f9c-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="46f9c-133">Aktivierungs Werte werden so lange beibehalten, bis der virtuelle Computer heruntergefahren oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="46f9c-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="46f9c-134">Beachten Sie, dass Windows Virtual PC die Konfiguration möglicherweise nur zum Speichern von Werten für bestimmte Schlüssel verwendet, d. h., der Aktivierungs Wert darf nie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46f9c-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="46f9c-135">Die Sitzung für virtuelle Computer muss ausgeführt werden, bevor Aktivierungs Werte geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="46f9c-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="46f9c-136">Aktivierungsschlüssel werden auf hierarchische Weise wie die Registrierungsschlüssel in Windows gespeichert.</span><span class="sxs-lookup"><span data-stu-id="46f9c-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="46f9c-137">Um einen bestimmten Unterschlüssel anzugeben, wird ein "Schlüssel Pfad" erstellt, der die verschiedenen Schlüssel in einem durch Trennzeichen getrennten Format angibt.</span><span class="sxs-lookup"><span data-stu-id="46f9c-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="46f9c-138">Um z. b. den Wert des Schlüssels "Default Action" zu entfernen, der \_ sich in der folgenden Schlüsselstruktur befindet:</span><span class="sxs-lookup"><span data-stu-id="46f9c-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="46f9c-139">Die Pfad Zeichenfolge von *activationkey* wird wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="46f9c-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="46f9c-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46f9c-140">Requirements</span></span>



| <span data-ttu-id="46f9c-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46f9c-141">Requirement</span></span> | <span data-ttu-id="46f9c-142">Wert</span><span class="sxs-lookup"><span data-stu-id="46f9c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f9c-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46f9c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="46f9c-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46f9c-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46f9c-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46f9c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="46f9c-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46f9c-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="46f9c-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="46f9c-147">End of client support</span></span><br/>    | <span data-ttu-id="46f9c-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46f9c-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="46f9c-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="46f9c-149">Product</span></span><br/>                  | <span data-ttu-id="46f9c-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46f9c-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="46f9c-151">Header</span><span class="sxs-lookup"><span data-stu-id="46f9c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="46f9c-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f9c-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="46f9c-153">IID</span><span class="sxs-lookup"><span data-stu-id="46f9c-153">IID</span></span><br/>                      | <span data-ttu-id="46f9c-154">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="46f9c-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="46f9c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46f9c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f9c-156">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="46f9c-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

