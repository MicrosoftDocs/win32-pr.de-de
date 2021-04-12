---
title: Ivmguestos multipleusersessionsallowed (Eigenschaft)
description: Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Multipleusersessionsallowed-Eigenschaft virtueller PC
- Multipleusersessionsallowed-Eigenschaft virtueller PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, multipleusersessionsallowed (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103970"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="c8d79-106">Ivmguestos:: multipleusersessionsallowed (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c8d79-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="c8d79-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8d79-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8d79-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8d79-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8d79-109">Bestimmt, ob mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c8d79-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="c8d79-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8d79-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d79-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d79-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="c8d79-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c8d79-112">Property value</span></span>

<span data-ttu-id="c8d79-113">**Variant \_ "True** ", wenn mehrere gleichzeitige Benutzersitzungen im Gast Betriebssystem zulässig sind, andernfalls " **\_ false** ".</span><span class="sxs-lookup"><span data-stu-id="c8d79-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8d79-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8d79-114">Error codes</span></span>



| <span data-ttu-id="c8d79-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c8d79-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="c8d79-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c8d79-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8d79-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8d79-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="c8d79-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8d79-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="c8d79-119"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c8d79-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="c8d79-120">Remotedesktopdienste (früher als "Terminal Services" bezeichnet) wurde noch nicht im Gast Betriebssystem initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c8d79-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="c8d79-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8d79-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="c8d79-122">Der *Sessionstatus* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c8d79-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="c8d79-123"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="c8d79-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="c8d79-124">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8d79-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="c8d79-125"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="c8d79-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="c8d79-126">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="c8d79-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="c8d79-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8d79-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="c8d79-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c8d79-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="c8d79-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d79-129">Remarks</span></span>

<span data-ttu-id="c8d79-130">Der Wert dieser Eigenschaft ist nur gültig, wenn die [**terminalservicesinitialized**](ivmguestos-terminalservicesinitialized.md) -Eigenschaft **Variant \_ true** ist.</span><span class="sxs-lookup"><span data-stu-id="c8d79-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="c8d79-131">Bei Windows-Client Betriebssystemen ist **multipleusersessionsallowed** **Variant \_ true** , wenn die schnelle Benutzerumschaltung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c8d79-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="c8d79-132">Bei Windows Server-Betriebssystemen ist **multipleusersessionsallowed** **Variant \_ true** , wenn Remotedesktopdienste (früher als "Terminal Services" bezeichnet) installiert und aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c8d79-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d79-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8d79-133">Requirements</span></span>



| <span data-ttu-id="c8d79-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8d79-134">Requirement</span></span> | <span data-ttu-id="c8d79-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c8d79-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d79-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8d79-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d79-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8d79-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8d79-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8d79-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d79-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8d79-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c8d79-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c8d79-140">End of client support</span></span><br/>    | <span data-ttu-id="c8d79-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8d79-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="c8d79-142">IDL</span><span class="sxs-lookup"><span data-stu-id="c8d79-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8d79-143"><dt>Ivmguestos. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8d79-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="c8d79-144">IID</span><span class="sxs-lookup"><span data-stu-id="c8d79-144">IID</span></span><br/>                      | <span data-ttu-id="c8d79-145">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="c8d79-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c8d79-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d79-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d79-147">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="c8d79-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

