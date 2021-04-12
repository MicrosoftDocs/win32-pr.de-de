---
title: Ivmguestos terminalserverport (Eigenschaft)
description: Port, der von Remotedesktopdienste im Gast Betriebssystem verwendet wird.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Terminalserverport-Eigenschaft virtueller PC
- Terminalserverport-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, terminalserverport (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105818"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="56c93-106">Ivmguestos:: terminalserverport-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56c93-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="56c93-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56c93-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56c93-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56c93-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56c93-109">Port, der von Remotedesktopdienste (früher als "Terminal Services" bezeichnet) im Gast Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56c93-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="56c93-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56c93-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c93-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c93-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="56c93-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56c93-112">Property value</span></span>

<span data-ttu-id="56c93-113">Gibt den Port zurück, der von Remotedesktopdienste im Gast Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56c93-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="56c93-114">Wert</span><span class="sxs-lookup"><span data-stu-id="56c93-114">Value</span></span>                                                                              | <span data-ttu-id="56c93-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56c93-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="56c93-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="56c93-117">Standardwert</span><span class="sxs-lookup"><span data-stu-id="56c93-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="56c93-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="56c93-119">Gültiger Bereich</span><span class="sxs-lookup"><span data-stu-id="56c93-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="56c93-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="56c93-121">Ein gültiger Portwert ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56c93-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="56c93-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="56c93-122">Error codes</span></span>



| <span data-ttu-id="56c93-123">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="56c93-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="56c93-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56c93-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56c93-125"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="56c93-126">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="56c93-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="56c93-127"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="56c93-128">Remotedesktopdienste wurde noch nicht im Gast Betriebssystem initialisiert.</span><span class="sxs-lookup"><span data-stu-id="56c93-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="56c93-129"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="56c93-130">Der *tsport* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="56c93-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="56c93-131"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="56c93-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="56c93-132">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56c93-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="56c93-133"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="56c93-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="56c93-134">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="56c93-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="56c93-135"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="56c93-136">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="56c93-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="56c93-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56c93-137">Remarks</span></span>

<span data-ttu-id="56c93-138">Der Wert dieser Eigenschaft ist nur gültig, wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft **Variant \_ true** ist.</span><span class="sxs-lookup"><span data-stu-id="56c93-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="56c93-139">Wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft aufgrund eines Verbindungsfehlers auf dem Port **Variant \_ false** ist, enthält der Wert, der von der Eigenschaft **terminalserverport** zurückgegeben wird, den Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="56c93-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c93-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56c93-140">Requirements</span></span>



| <span data-ttu-id="56c93-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c93-141">Requirement</span></span> | <span data-ttu-id="56c93-142">Wert</span><span class="sxs-lookup"><span data-stu-id="56c93-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c93-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56c93-143">Minimum supported client</span></span><br/> | <span data-ttu-id="56c93-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56c93-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56c93-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56c93-145">Minimum supported server</span></span><br/> | <span data-ttu-id="56c93-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="56c93-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="56c93-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="56c93-147">End of client support</span></span><br/>    | <span data-ttu-id="56c93-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56c93-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="56c93-149">IDL</span><span class="sxs-lookup"><span data-stu-id="56c93-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56c93-150"><dt>Ivmguestos. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56c93-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="56c93-151">IID</span><span class="sxs-lookup"><span data-stu-id="56c93-151">IID</span></span><br/>                      | <span data-ttu-id="56c93-152">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="56c93-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="56c93-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c93-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c93-154">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="56c93-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

