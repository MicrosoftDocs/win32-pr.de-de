---
title: Ivmvirtualmachine shutdownaktiononquit-Eigenschaft (vpccominterfaces. h)
description: Aktion, die auf dieser virtuellen Maschine ausgeführt werden soll, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Shutdownaktiononquit-Eigenschaft, virtueller PC
- Shutdownaktiononquit-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, shutdownaktiononquit (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478330"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="cf666-106">Ivmvirtualmachine:: shutdownaktiononquit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cf666-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="cf666-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf666-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cf666-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cf666-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cf666-109">Ruft die Aktion ab, die auf diesem virtuellen Computer (VM) ausgeführt wird, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="cf666-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="cf666-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cf666-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf666-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf666-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="cf666-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cf666-112">Property value</span></span>

<span data-ttu-id="cf666-113">Gibt an, wie diese VM heruntergefahren wird, wenn Sie ausgeführt wird, wenn Windows Virtual PC beendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf666-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="cf666-114">Eine Liste der Werte finden Sie unter [**vmshutdownaction**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="cf666-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf666-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cf666-115">Error codes</span></span>



| <span data-ttu-id="cf666-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="cf666-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cf666-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cf666-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf666-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cf666-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf666-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cf666-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cf666-121">Der-Parameter ist **null** oder kein gültiger-Wert.</span><span class="sxs-lookup"><span data-stu-id="cf666-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="cf666-122"><dt>E \_ AccessDenied</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="cf666-123">Der aktuelle Benutzer verfügt nicht über ausreichenden Zugriff auf die Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="cf666-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="cf666-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="cf666-125">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="cf666-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cf666-126"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cf666-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cf666-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="cf666-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf666-128">Remarks</span></span>

<span data-ttu-id="cf666-129">Standardmäßig werden virtuelle Computer, die ausgeführt werden, beim Beenden von Windows Virtual PC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cf666-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="cf666-130">Durch die Aktion zum herunter **fahren ( \_ 0** ) wird der Zustand der VM gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cf666-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="cf666-131">Mit der Aktion " **vmshutdownaction \_ Turnoff** (1)" wird der virtuelle Computer ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="cf666-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="cf666-132">Durch die Aktion zum **\_ Herunterfahren von vmshutdownaction** (2) wird das Gast Betriebssystem heruntergefahren, wenn die Integrations Komponenten verfügbar sind, und andernfalls wird die VM gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cf666-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf666-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf666-133">Requirements</span></span>



| <span data-ttu-id="cf666-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf666-134">Requirement</span></span> | <span data-ttu-id="cf666-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cf666-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf666-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf666-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cf666-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf666-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf666-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf666-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cf666-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cf666-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cf666-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cf666-140">End of client support</span></span><br/>    | <span data-ttu-id="cf666-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf666-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cf666-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="cf666-142">Product</span></span><br/>                  | <span data-ttu-id="cf666-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cf666-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cf666-144">Header</span><span class="sxs-lookup"><span data-stu-id="cf666-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf666-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf666-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cf666-146">IID</span><span class="sxs-lookup"><span data-stu-id="cf666-146">IID</span></span><br/>                      | <span data-ttu-id="cf666-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="cf666-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cf666-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf666-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf666-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="cf666-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="cf666-150">**Vmshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="cf666-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

