---
title: Ivmguestos isheartangeschlagen-Eigenschaft (vpccominterfaces. h)
description: Bestimmt, ob der virtuelle Computer über einen Takt verfügt.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Isheartangeschlagen-Eigenschaft virtueller PC
- Isheartangeschlagen-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, isheartangeschlagen (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342666"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="e6e88-106">Ivmguestos:: isheartangeschlagen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e6e88-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="e6e88-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6e88-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6e88-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6e88-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6e88-109">Bestimmt, ob der virtuelle Computer über einen Takt verfügt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="e6e88-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e88-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6e88-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="e6e88-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e6e88-112">Property value</span></span>

<span data-ttu-id="e6e88-113">**Variant \_ "True** ", wenn ein Takt erkannt wird, andernfalls " **\_ false** ".</span><span class="sxs-lookup"><span data-stu-id="e6e88-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6e88-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e6e88-114">Error codes</span></span>



| <span data-ttu-id="e6e88-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e6e88-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="e6e88-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e6e88-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6e88-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="e6e88-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="e6e88-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="e6e88-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e6e88-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="e6e88-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="e6e88-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="e6e88-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="e6e88-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="e6e88-124">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e6e88-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="e6e88-125"><dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="e6e88-126">Der virtuelle Computer wurde nicht vollständig gestartet, das Feature für die Integrations Komponenten ist nicht installiert, oder die installierte Version unterstützt diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="e6e88-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="e6e88-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="e6e88-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e6e88-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="e6e88-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6e88-129">Remarks</span></span>

<span data-ttu-id="e6e88-130">Wenn Integrations Komponenten im Gast Betriebssystem installiert sind, wird ein regulärer Takt oder Takt von der Sitzung der virtuellen Maschine an Windows Virtual PC gesendet.</span><span class="sxs-lookup"><span data-stu-id="e6e88-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="e6e88-131">Wenn das Gast Betriebssystem stark ausgelastet ist, wird es möglich sein, dass der virtuelle PC weniger Takte als erwartet empfängt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="e6e88-132">Wenn kein Takt erkannt wird, reagiert das Gast Betriebssystem möglicherweise nicht oder ist abgestürzt.</span><span class="sxs-lookup"><span data-stu-id="e6e88-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="e6e88-133">Standardmäßig erzeugt ein virtueller Computer zehn Takt Ticks pro Minute.</span><span class="sxs-lookup"><span data-stu-id="e6e88-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="e6e88-134">Wenn für eine ganze Minute keine Takt Takte erkannt werden, versucht Windows Virtual PC, die Sitzung für virtuelle Maschinen alle zehn Sekunden bis zu zwei Minuten neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="e6e88-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="e6e88-135">Dieses Verhalten wird durch die folgenden Schlüsselwerte in der Konfigurationsdatei der Sitzung der virtuellen Maschine gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e6e88-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="e6e88-136">Konfigurationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="e6e88-136">Configuration key</span></span>                                            | <span data-ttu-id="e6e88-137">Standard</span><span class="sxs-lookup"><span data-stu-id="e6e88-137">Default</span></span>       | <span data-ttu-id="e6e88-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6e88-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e88-139">Integration/Microsoft/Heartbeat/Zeit</span><span class="sxs-lookup"><span data-stu-id="e6e88-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="e6e88-140">60</span><span class="sxs-lookup"><span data-stu-id="e6e88-140">60</span></span><br/> | <span data-ttu-id="e6e88-141">Die Länge des Zeit Blocks, der zum Generieren von Takt Ticks verwendet wird (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="e6e88-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="e6e88-142">Integration/Microsoft/Heartbeat/Rate</span><span class="sxs-lookup"><span data-stu-id="e6e88-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="e6e88-143">10</span><span class="sxs-lookup"><span data-stu-id="e6e88-143">10</span></span><br/> | <span data-ttu-id="e6e88-144">Die Anzahl der Ticks, die in jedem Takt Zeit Block generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e6e88-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="e6e88-145">Integration/Microsoft/Heartbeat/Fehler \_ Intervall</span><span class="sxs-lookup"><span data-stu-id="e6e88-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="e6e88-146">10</span><span class="sxs-lookup"><span data-stu-id="e6e88-146">10</span></span><br/> | <span data-ttu-id="e6e88-147">Die Anzahl der Sekunden zwischen Neustart versuchen, sobald keine Takt Ticks innerhalb eines bestimmten Takt Zeit Blocks empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="e6e88-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="e6e88-148">Integration/Microsoft/Heartbeat/Fehler \_ Versuche</span><span class="sxs-lookup"><span data-stu-id="e6e88-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="e6e88-149">12</span><span class="sxs-lookup"><span data-stu-id="e6e88-149">12</span></span><br/> | <span data-ttu-id="e6e88-150">Die Anzahl der erfolgten Neustart Versuche.</span><span class="sxs-lookup"><span data-stu-id="e6e88-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="e6e88-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e88-151">Requirements</span></span>



| <span data-ttu-id="e6e88-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e88-152">Requirement</span></span> | <span data-ttu-id="e6e88-153">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e88-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e88-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e88-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e88-155">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e88-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6e88-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6e88-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e88-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e6e88-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6e88-158">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e88-158">End of client support</span></span><br/>    | <span data-ttu-id="e6e88-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6e88-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6e88-160">Produkt</span><span class="sxs-lookup"><span data-stu-id="e6e88-160">Product</span></span><br/>                  | <span data-ttu-id="e6e88-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6e88-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6e88-162">Header</span><span class="sxs-lookup"><span data-stu-id="e6e88-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e88-163"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e88-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6e88-164">IID</span><span class="sxs-lookup"><span data-stu-id="e6e88-164">IID</span></span><br/>                      | <span data-ttu-id="e6e88-165">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="e6e88-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e6e88-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e88-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e88-167">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="e6e88-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

