---
title: Ivmvirtualmachine UndoAction-Eigenschaft (vpccominterfaces. h)
description: Standardaktion, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer heruntergefahren wird.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction-Eigenschaft virtueller PC
- UndoAction-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, UndoAction-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478321"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="4f1b4-106">Ivmvirtualmachine:: UndoAction (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="4f1b4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4f1b4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4f1b4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4f1b4-109">Hiermit wird die Standardaktion abgerufen und festgelegt, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer mithilfe der [**Turnoff**](ivmvirtualmachine-turnoff.md) -Methode ausgeschaltet oder mithilfe der [**Shutdown**](ivmguestos-shutdown.md) -Methode heruntergefahren oder innerhalb des Gast Betriebssystems ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="4f1b4-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1b4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f1b4-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="4f1b4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4f1b4-112">Property value</span></span>

<span data-ttu-id="4f1b4-113">Gibt die Standardaktion an, die auf allen rückgängig-Laufwerken ausgeführt werden soll, wenn der virtuelle Computer innerhalb des Gast Betriebssystems heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="4f1b4-114">Eine Liste der Werte finden Sie unter [**vmundoaction**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="4f1b4-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f1b4-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4f1b4-115">Error codes</span></span>



| <span data-ttu-id="4f1b4-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="4f1b4-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4f1b4-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4f1b4-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4f1b4-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4f1b4-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4f1b4-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4f1b4-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4f1b4-122"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="4f1b4-123">Der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="4f1b4-124"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4f1b4-125">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="4f1b4-126"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4f1b4-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4f1b4-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f1b4-128">Requirements</span></span>



| <span data-ttu-id="4f1b4-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f1b4-129">Requirement</span></span> | <span data-ttu-id="4f1b4-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4f1b4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1b4-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1b4-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f1b4-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f1b4-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1b4-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4f1b4-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4f1b4-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4f1b4-135">End of client support</span></span><br/>    | <span data-ttu-id="4f1b4-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f1b4-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4f1b4-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="4f1b4-137">Product</span></span><br/>                  | <span data-ttu-id="4f1b4-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4f1b4-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4f1b4-139">Header</span><span class="sxs-lookup"><span data-stu-id="4f1b4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1b4-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b4-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4f1b4-141">IID</span><span class="sxs-lookup"><span data-stu-id="4f1b4-141">IID</span></span><br/>                      | <span data-ttu-id="4f1b4-142">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="4f1b4-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4f1b4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f1b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1b4-144">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="4f1b4-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

