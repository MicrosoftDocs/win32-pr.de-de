---
title: Ivmguestos heartbeatprozent-Eigenschaft (vpccominterfaces. h)
description: Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Eigenschaft "heartbeatprozent" für Virtual PC
- Eigenschaft "heartbeatprozent" Virtual PC, ivmguestos Interface
- Ivmguestos Interface Virtual PC, Eigenschaft "heartbeatprozentsatz"
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518800"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="c76e7-106">Ivmguestos:: heartbeatprozent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c76e7-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="c76e7-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c76e7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c76e7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c76e7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c76e7-109">Ruft den Prozentsatz der erwarteten Takte ab, die in der letzten Minute empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c76e7-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="c76e7-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c76e7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76e7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c76e7-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="c76e7-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c76e7-112">Property value</span></span>

<span data-ttu-id="c76e7-113">Der Prozentsatz der erwarteten Takte, die in der letzten Minute empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c76e7-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c76e7-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c76e7-114">Error codes</span></span>



| <span data-ttu-id="c76e7-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c76e7-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="c76e7-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c76e7-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c76e7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="c76e7-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c76e7-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="c76e7-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="c76e7-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c76e7-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="c76e7-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="c76e7-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c76e7-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="c76e7-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="c76e7-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="c76e7-124">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c76e7-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="c76e7-125"><dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="c76e7-126">Der virtuelle Computer wurde nicht vollständig gestartet, das Feature für die Integrations Komponenten ist nicht installiert, oder die installierte Version unterstützt diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="c76e7-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="c76e7-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="c76e7-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c76e7-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="c76e7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c76e7-129">Remarks</span></span>

<span data-ttu-id="c76e7-130">Integrations Komponenten senden regelmäßig Taktfrequenz an Windows Virtual PC, während das Gast Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c76e7-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="c76e7-131">Wenn das Gast Betriebssystem stark ausgelastet ist, wird es möglich sein, dass Windows Virtual PC weniger Takte als erwartet empfängt.</span><span class="sxs-lookup"><span data-stu-id="c76e7-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="c76e7-132">Fällt der Takt Prozentsatz auf NULL, ist es möglich, dass das Gast Betriebssystem nicht reagiert oder abgestürzt ist.</span><span class="sxs-lookup"><span data-stu-id="c76e7-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="c76e7-133">Der virtuelle Computer muss ausgeführt werden (d. h. vollständig gestartet und nicht heruntergefahren werden), und Integrations Komponenten müssen installiert werden, wenn diese Eigenschaft aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c76e7-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76e7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c76e7-134">Requirements</span></span>



| <span data-ttu-id="c76e7-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c76e7-135">Requirement</span></span> | <span data-ttu-id="c76e7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c76e7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c76e7-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c76e7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c76e7-138">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c76e7-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c76e7-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c76e7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c76e7-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c76e7-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c76e7-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c76e7-141">End of client support</span></span><br/>    | <span data-ttu-id="c76e7-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c76e7-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c76e7-143">Produkt</span><span class="sxs-lookup"><span data-stu-id="c76e7-143">Product</span></span><br/>                  | <span data-ttu-id="c76e7-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c76e7-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c76e7-145">Header</span><span class="sxs-lookup"><span data-stu-id="c76e7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c76e7-146"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76e7-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c76e7-147">IID</span><span class="sxs-lookup"><span data-stu-id="c76e7-147">IID</span></span><br/>                      | <span data-ttu-id="c76e7-148">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="c76e7-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c76e7-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c76e7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76e7-150">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="c76e7-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

