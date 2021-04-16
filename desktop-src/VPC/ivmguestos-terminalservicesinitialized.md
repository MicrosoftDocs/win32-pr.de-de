---
title: Ivmguestos terminalservicesinitialized-Eigenschaft (vpccominterfaces. h)
description: Status der Remotedesktopdienste im Gast Betriebssystem.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Terminalservicesinitialized-Eigenschaft virtueller PC
- Terminalservicesinitialized-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, terminalservicesinitialized (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518917"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="a8a27-106">Ivmguestos:: terminalservicesinitialized-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a8a27-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="a8a27-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8a27-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a8a27-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a8a27-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a8a27-109">Ruft den Status Remotedesktopdienste (früher als "Terminal Services" bezeichnet) im Gast Betriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="a8a27-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="a8a27-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a8a27-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a27-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8a27-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="a8a27-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a8a27-112">Property value</span></span>

<span data-ttu-id="a8a27-113">Der Initialisierungs Status.</span><span class="sxs-lookup"><span data-stu-id="a8a27-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8a27-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a8a27-114">Error codes</span></span>



| <span data-ttu-id="a8a27-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a8a27-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a8a27-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a8a27-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8a27-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a8a27-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a8a27-118">Der Vorgang war erfolgreich, und Remotedesktopdienste wurde initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a8a27-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="a8a27-119">Der zurückgegebene Eigenschafts Wert gibt an, ob Remotedesktopdienste im Gast Betriebssystem verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a8a27-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="a8a27-120"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a8a27-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="a8a27-121">Die Funktion "Integrations Komponenten" wird ausgeführt, aber Remotedesktopdienste noch nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a8a27-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="a8a27-122"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a8a27-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="a8a27-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a8a27-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="a8a27-124"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="a8a27-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="a8a27-125">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a8a27-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="a8a27-126"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="a8a27-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="a8a27-127">Das Feature "Integrations Komponenten" wird nicht im Gast Betriebssystem ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8a27-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="a8a27-128"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a8a27-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a8a27-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a8a27-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="a8a27-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8a27-130">Requirements</span></span>



| <span data-ttu-id="a8a27-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8a27-131">Requirement</span></span> | <span data-ttu-id="a8a27-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a8a27-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a27-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8a27-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a27-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8a27-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8a27-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8a27-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a27-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8a27-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a8a27-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a8a27-137">End of client support</span></span><br/>    | <span data-ttu-id="a8a27-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8a27-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a8a27-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="a8a27-139">Product</span></span><br/>                  | <span data-ttu-id="a8a27-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a8a27-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a8a27-141">Header</span><span class="sxs-lookup"><span data-stu-id="a8a27-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a27-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a27-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a8a27-143">IID</span><span class="sxs-lookup"><span data-stu-id="a8a27-143">IID</span></span><br/>                      | <span data-ttu-id="a8a27-144">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="a8a27-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a8a27-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8a27-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a27-146">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="a8a27-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

