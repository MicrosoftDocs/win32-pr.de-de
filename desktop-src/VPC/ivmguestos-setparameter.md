---
title: Ivmguestos SetParameter-Methode (vpccominterfaces. h)
description: Legt einen benannten Parameter innerhalb des Gast Betriebssystems fest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- SetParameter-Methode Virtual PC
- SetParameter-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, SetParameter-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517897"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="b197d-106">Ivmguestos:: SetParameter-Methode</span><span class="sxs-lookup"><span data-stu-id="b197d-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="b197d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b197d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b197d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b197d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b197d-109">Legt einen benannten Parameter innerhalb des Gast Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="b197d-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b197d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b197d-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="b197d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b197d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b197d-112">*inparametername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b197d-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b197d-113">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="b197d-113">The parameter name.</span></span> <span data-ttu-id="b197d-114">Der Wert muss zwischen 1 und 255 Zeichen lang sein und darf keinen umgekehrten Schrägstrich ( \) Zeichen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b197d-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="b197d-115">*inparametervalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b197d-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b197d-116">Der Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="b197d-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b197d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b197d-117">Return value</span></span>

<span data-ttu-id="b197d-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b197d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="b197d-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b197d-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="b197d-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b197d-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b197d-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="b197d-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b197d-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="b197d-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="b197d-124">Ein Parameter ist ungültig oder wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b197d-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="b197d-125"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="b197d-126">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="b197d-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="b197d-127"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="b197d-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="b197d-128">Der virtuelle Computer (VM) wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b197d-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="b197d-129"><dt>**VM \_ E- \_ VM \_ angeh**</dt> alten <dt>0xa00400507</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="b197d-130">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="b197d-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b197d-131"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="b197d-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="b197d-132">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="b197d-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="b197d-133"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="b197d-134">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b197d-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b197d-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b197d-135">Remarks</span></span>

<span data-ttu-id="b197d-136">Der virtuelle Computer muss ausgeführt werden, und Integrations Komponenten müssen installiert werden, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b197d-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="b197d-137">Diese Methode wird nur für Windows-basierte Gast Betriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b197d-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="b197d-138">Wenn Integrations Komponenten installiert sind, wird der folgende Schlüssel der Registrierung des Gast Betriebssystems automatisch hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b197d-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="b197d-139">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="b197d-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="b197d-140">Wenn das Gast Betriebssystem gestartet wird, werden die folgenden Registrierungszeichen folgen Werte im **Parameter** Schlüssel aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="b197d-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="b197d-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="b197d-141">**HostName**</span></span>
-   <span data-ttu-id="b197d-142">**Physicalhostname**</span><span class="sxs-lookup"><span data-stu-id="b197d-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="b197d-143">**Physicalhostnamefullyqualified**</span><span class="sxs-lookup"><span data-stu-id="b197d-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="b197d-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="b197d-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="b197d-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b197d-145">Requirements</span></span>



| <span data-ttu-id="b197d-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b197d-146">Requirement</span></span> | <span data-ttu-id="b197d-147">Wert</span><span class="sxs-lookup"><span data-stu-id="b197d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b197d-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b197d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b197d-149">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b197d-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b197d-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b197d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b197d-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b197d-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b197d-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b197d-152">End of client support</span></span><br/>    | <span data-ttu-id="b197d-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b197d-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b197d-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="b197d-154">Product</span></span><br/>                  | <span data-ttu-id="b197d-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b197d-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b197d-156">Header</span><span class="sxs-lookup"><span data-stu-id="b197d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b197d-157"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b197d-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b197d-158">IID</span><span class="sxs-lookup"><span data-stu-id="b197d-158">IID</span></span><br/>                      | <span data-ttu-id="b197d-159">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="b197d-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b197d-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b197d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b197d-161">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="b197d-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

