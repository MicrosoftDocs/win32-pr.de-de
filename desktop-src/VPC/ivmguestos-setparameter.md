---
title: IVMGuestOS SetParameter-Methode (VPCCOMInterfaces.h)
description: Legt einen benannten Parameter innerhalb des Gastbetriebssystems fest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- 'SetParameter-Methode : Virtueller PC'
- SetParameter-Methode Virtual PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, SetParameter-Methode
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
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386709"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="91e4b-106">IVMGuestOS::SetParameter-Methode</span><span class="sxs-lookup"><span data-stu-id="91e4b-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="91e4b-107">\[Der virtuelle Windows-PC kann ab diesem Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91e4b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91e4b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="91e4b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91e4b-109">Legt einen benannten Parameter innerhalb des Gastbetriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="91e4b-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e4b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e4b-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="91e4b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e4b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e4b-112">*inParameterName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="91e4b-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e4b-113">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="91e4b-113">The parameter name.</span></span> <span data-ttu-id="91e4b-114">Er muss zwischen 1 und 255 Zeichen lang sein und darf keinen schrägen Schrägstrich \\ () enthalten.</span><span class="sxs-lookup"><span data-stu-id="91e4b-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="91e4b-115">*inParameterValue* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="91e4b-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e4b-116">Der Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="91e4b-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e4b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91e4b-117">Return value</span></span>

<span data-ttu-id="91e4b-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91e4b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="91e4b-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="91e4b-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="91e4b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91e4b-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="91e4b-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="91e4b-122">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="91e4b-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="91e4b-123"><dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="91e4b-124">Ein Parameter ist ungültig oder nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="91e4b-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="91e4b-125"><dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="91e4b-126">Der Vorgang wurde nicht rechtzeitig abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="91e4b-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="91e4b-127"><dt>**VM \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="91e4b-128">Der virtuelle Computer (VM) wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91e4b-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="91e4b-129"><dt>**VM \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="91e4b-130">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="91e4b-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="91e4b-131"><dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="91e4b-132">Integrationskomponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="91e4b-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="91e4b-133"><dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="91e4b-134">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="91e4b-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="91e4b-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91e4b-135">Remarks</span></span>

<span data-ttu-id="91e4b-136">Die VM muss ausgeführt werden, und Integrationskomponenten müssen installiert werden, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="91e4b-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="91e4b-137">Diese Methode wird nur für Windows-basierte Gastbetriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91e4b-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="91e4b-138">Wenn Integrationskomponenten installiert sind, wird der folgende Schlüssel automatisch zur Registrierung des Gastbetriebssystems hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="91e4b-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="91e4b-139">**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**</span><span class="sxs-lookup"><span data-stu-id="91e4b-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="91e4b-140">Wenn das Gastbetriebssystem gestartet wird, werden die folgenden Registrierungszeichenfolgenwerte im Schlüssel **Parameter aufgefüllt:**</span><span class="sxs-lookup"><span data-stu-id="91e4b-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="91e4b-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="91e4b-141">**HostName**</span></span>
-   <span data-ttu-id="91e4b-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="91e4b-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="91e4b-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="91e4b-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="91e4b-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="91e4b-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="91e4b-145">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="91e4b-145">Requirements</span></span>



| <span data-ttu-id="91e4b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91e4b-146">Requirement</span></span> | <span data-ttu-id="91e4b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="91e4b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e4b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91e4b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="91e4b-149">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91e4b-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91e4b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91e4b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="91e4b-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="91e4b-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91e4b-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="91e4b-152">End of client support</span></span><br/>    | <span data-ttu-id="91e4b-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91e4b-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91e4b-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="91e4b-154">Product</span></span><br/>                  | <span data-ttu-id="91e4b-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91e4b-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91e4b-156">Header</span><span class="sxs-lookup"><span data-stu-id="91e4b-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e4b-157"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91e4b-158">IID</span><span class="sxs-lookup"><span data-stu-id="91e4b-158">IID</span></span><br/>                      | <span data-ttu-id="91e4b-159">IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="91e4b-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="91e4b-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91e4b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e4b-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="91e4b-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

