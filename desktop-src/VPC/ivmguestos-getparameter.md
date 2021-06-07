---
title: IVMGuestOS GetParameter-Methode (VPCCOMInterfaces.h)
description: Ruft einen benannten Parameter im Gastbetriebssystem ab.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter-Methode Virtueller PC
- GetParameter-Methode Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, GetParameter-Methode
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
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387646"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="bdadd-106">IVMGuestOS::GetParameter-Methode</span><span class="sxs-lookup"><span data-stu-id="bdadd-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="bdadd-107">\[Windows Virtual PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdadd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bdadd-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="bdadd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bdadd-109">Ruft einen benannten Parameter im Gastbetriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="bdadd-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdadd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdadd-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="bdadd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdadd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdadd-112">*inParameterName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bdadd-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadd-113">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="bdadd-113">The parameter name.</span></span> <span data-ttu-id="bdadd-114">Er muss zwischen 1 und 255 Zeichen lang sein und darf keinen umgekehrten Schrägstrich \\ () enthalten.</span><span class="sxs-lookup"><span data-stu-id="bdadd-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="bdadd-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bdadd-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bdadd-116">Der Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="bdadd-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdadd-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdadd-117">Return value</span></span>

<span data-ttu-id="bdadd-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bdadd-118">This method can return one of these values.</span></span>



| <span data-ttu-id="bdadd-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bdadd-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="bdadd-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdadd-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdadd-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="bdadd-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdadd-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="bdadd-123"><dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="bdadd-124">Ein Parameter ist ungültig oder nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="bdadd-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="bdadd-125"><dt>**E \_ POINTER**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="bdadd-126">Der Parameter ist **NULL.**</span><span class="sxs-lookup"><span data-stu-id="bdadd-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="bdadd-127"><dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="bdadd-128">Der Vorgang wurde nicht rechtzeitig abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="bdadd-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="bdadd-129"><dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="bdadd-130">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdadd-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="bdadd-131"><dt>**VM \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="bdadd-132">Der virtuelle Computer wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="bdadd-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bdadd-133"><dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="bdadd-134">Integrationskomponenten werden auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="bdadd-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="bdadd-135"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="bdadd-136">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bdadd-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="bdadd-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdadd-137">Remarks</span></span>

<span data-ttu-id="bdadd-138">Der virtuelle Computer muss ausgeführt werden, und Integrationskomponenten müssen installiert werden, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bdadd-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="bdadd-139">Diese Methode wird nur für Windows-basierte Gastbetriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdadd-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="bdadd-140">Bei installierten Integrationskomponenten wird der Registrierung des Gastbetriebssystems automatisch der folgende Schlüssel hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bdadd-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="bdadd-141">**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="bdadd-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="bdadd-142">Wenn das Gastbetriebssystem gestartet wird, werden die folgenden Werte der Registrierungszeichenfolge im **Parameterschlüssel** aufgefüllt:</span><span class="sxs-lookup"><span data-stu-id="bdadd-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="bdadd-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="bdadd-143">**HostName**</span></span>
-   <span data-ttu-id="bdadd-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="bdadd-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="bdadd-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="bdadd-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="bdadd-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="bdadd-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="bdadd-147">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bdadd-147">Requirements</span></span>



| <span data-ttu-id="bdadd-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdadd-148">Requirement</span></span> | <span data-ttu-id="bdadd-149">Wert</span><span class="sxs-lookup"><span data-stu-id="bdadd-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdadd-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdadd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bdadd-151">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdadd-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bdadd-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdadd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bdadd-153">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bdadd-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bdadd-154">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bdadd-154">End of client support</span></span><br/>    | <span data-ttu-id="bdadd-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bdadd-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bdadd-156">Produkt</span><span class="sxs-lookup"><span data-stu-id="bdadd-156">Product</span></span><br/>                  | <span data-ttu-id="bdadd-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bdadd-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bdadd-158">Header</span><span class="sxs-lookup"><span data-stu-id="bdadd-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdadd-159"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="bdadd-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bdadd-160">IID</span><span class="sxs-lookup"><span data-stu-id="bdadd-160">IID</span></span><br/>                      | <span data-ttu-id="bdadd-161">IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="bdadd-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bdadd-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdadd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdadd-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="bdadd-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

