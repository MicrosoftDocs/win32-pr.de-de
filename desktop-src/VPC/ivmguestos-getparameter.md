---
title: Ivmguestos GetParameter-Methode (vpccominterfaces. h)
description: Ruft einen benannten Parameter innerhalb des Gast Betriebssystems ab.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter-Methode Virtual PC
- GetParameter-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, GetParameter-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518797"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="27100-106">Ivmguestos:: GetParameter-Methode</span><span class="sxs-lookup"><span data-stu-id="27100-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="27100-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27100-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27100-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27100-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27100-109">Ruft einen benannten Parameter innerhalb des Gast Betriebssystems ab.</span><span class="sxs-lookup"><span data-stu-id="27100-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="27100-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="27100-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="27100-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="27100-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27100-112">*inparametername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27100-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27100-113">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="27100-113">The parameter name.</span></span> <span data-ttu-id="27100-114">Der Wert muss zwischen 1 und 255 Zeichen lang sein und darf keinen umgekehrten Schrägstrich ( \) Zeichen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="27100-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="27100-115">*outparametervalue* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27100-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27100-116">Der Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="27100-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27100-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27100-117">Return value</span></span>

<span data-ttu-id="27100-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="27100-118">This method can return one of these values.</span></span>



| <span data-ttu-id="27100-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="27100-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="27100-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27100-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27100-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27100-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="27100-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="27100-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="27100-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="27100-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="27100-124">Ein Parameter ist ungültig oder wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="27100-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="27100-125"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27100-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="27100-126">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="27100-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="27100-127"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="27100-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="27100-128">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="27100-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="27100-129"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="27100-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="27100-130">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27100-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="27100-131"><dt>**VM \_ E- \_ VM \_ angeh**</dt> alten <dt>0xa00400507</dt></span><span class="sxs-lookup"><span data-stu-id="27100-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="27100-132">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="27100-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="27100-133"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="27100-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="27100-134">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="27100-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="27100-135"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="27100-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="27100-136">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="27100-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="27100-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27100-137">Remarks</span></span>

<span data-ttu-id="27100-138">Der virtuelle Computer muss ausgeführt werden, und Integrations Komponenten müssen installiert werden, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="27100-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="27100-139">Diese Methode wird nur für Windows-basierte Gast Betriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27100-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="27100-140">Wenn Integrations Komponenten installiert sind, wird der folgende Schlüssel der Registrierung des Gast Betriebssystems automatisch hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="27100-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="27100-141">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="27100-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="27100-142">Wenn das Gast Betriebssystem gestartet wird, werden die folgenden Registrierungszeichen folgen Werte im **Parameter** Schlüssel aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="27100-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="27100-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="27100-143">**HostName**</span></span>
-   <span data-ttu-id="27100-144">**Physicalhostname**</span><span class="sxs-lookup"><span data-stu-id="27100-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="27100-145">**Physicalhostnamefullyqualified**</span><span class="sxs-lookup"><span data-stu-id="27100-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="27100-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="27100-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="27100-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27100-147">Requirements</span></span>



| <span data-ttu-id="27100-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27100-148">Requirement</span></span> | <span data-ttu-id="27100-149">Wert</span><span class="sxs-lookup"><span data-stu-id="27100-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27100-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27100-150">Minimum supported client</span></span><br/> | <span data-ttu-id="27100-151">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27100-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27100-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27100-152">Minimum supported server</span></span><br/> | <span data-ttu-id="27100-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27100-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27100-154">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="27100-154">End of client support</span></span><br/>    | <span data-ttu-id="27100-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27100-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27100-156">Produkt</span><span class="sxs-lookup"><span data-stu-id="27100-156">Product</span></span><br/>                  | <span data-ttu-id="27100-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27100-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27100-158">Header</span><span class="sxs-lookup"><span data-stu-id="27100-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="27100-159"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27100-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27100-160">IID</span><span class="sxs-lookup"><span data-stu-id="27100-160">IID</span></span><br/>                      | <span data-ttu-id="27100-161">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="27100-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="27100-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27100-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27100-163">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="27100-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

