---
title: Ivmguestos screenlocked-Eigenschaft (vpccominterfaces. h)
description: Gibt an, ob der Bildschirm im Gast Betriebssystem gesperrt ist.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Screenlocked-Eigenschaft virtueller PC
- Screenlocked-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, screenlocked (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040708"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="c8f22-106">Ivmguestos:: screenlocked (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c8f22-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="c8f22-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8f22-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8f22-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8f22-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8f22-109">Gibt an, ob der Bildschirm im Gast Betriebssystem gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="c8f22-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="c8f22-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8f22-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f22-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f22-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="c8f22-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c8f22-112">Property value</span></span>

<span data-ttu-id="c8f22-113">**Variant \_ "True** ", wenn der Bildschirm im Gast Betriebssystem gesperrt ist, andernfalls " **\_ false** ".</span><span class="sxs-lookup"><span data-stu-id="c8f22-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8f22-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8f22-114">Error codes</span></span>



| <span data-ttu-id="c8f22-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c8f22-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="c8f22-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c8f22-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8f22-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8f22-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="c8f22-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8f22-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="c8f22-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8f22-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="c8f22-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c8f22-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="c8f22-121"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="c8f22-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="c8f22-122">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f22-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="c8f22-123"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="c8f22-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="c8f22-124">Das Feature "Integrations Komponenten" ist nicht im Gast Betriebssystem aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8f22-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="c8f22-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8f22-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="c8f22-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c8f22-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="c8f22-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8f22-127">Requirements</span></span>



| <span data-ttu-id="c8f22-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8f22-128">Requirement</span></span> | <span data-ttu-id="c8f22-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c8f22-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f22-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8f22-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f22-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8f22-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8f22-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8f22-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f22-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8f22-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8f22-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c8f22-134">End of client support</span></span><br/>    | <span data-ttu-id="c8f22-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8f22-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8f22-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="c8f22-136">Product</span></span><br/>                  | <span data-ttu-id="c8f22-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8f22-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8f22-138">Header</span><span class="sxs-lookup"><span data-stu-id="c8f22-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f22-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f22-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8f22-140">IID</span><span class="sxs-lookup"><span data-stu-id="c8f22-140">IID</span></span><br/>                      | <span data-ttu-id="c8f22-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="c8f22-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c8f22-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8f22-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f22-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="c8f22-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

