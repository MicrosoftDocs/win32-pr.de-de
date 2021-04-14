---
title: Ivmvirtualmachine-Tastatur Eigenschaft (vpccominterfaces. h)
description: Ruft das Tastatur Gerät für den virtuellen Computer ab.
ms.assetid: bf516d07-eea9-40e3-b0d3-0fd4d3a04eb1
keywords:
- Tastatur Eigenschaft Virtual PC
- Tastatur Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Tastatur Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Keyboard
- IVMVirtualMachine.get_Keyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31080b376a9e0fa999d568e5f3c7524d597aa0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341068"
---
# <a name="ivmvirtualmachinekeyboard-property"></a><span data-ttu-id="a09ab-106">Ivmvirtualmachine:: Keyboard (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a09ab-106">IVMVirtualMachine::Keyboard property</span></span>

<span data-ttu-id="a09ab-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a09ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a09ab-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a09ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a09ab-109">Ruft das Tastatur Gerät für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="a09ab-109">Retrieves the keyboard device for the virtual machine.</span></span>

<span data-ttu-id="a09ab-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a09ab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09ab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a09ab-111">Syntax</span></span>


```C++
HRESULT get_Keyboard(
  [out, retval] IVMKeyboard **keyboard
);
```



## <a name="property-value"></a><span data-ttu-id="a09ab-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a09ab-112">Property value</span></span>

<span data-ttu-id="a09ab-113">Das [**ivmkeyboard**](ivmkeyboard.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a09ab-113">The [**IVMKeyboard**](ivmkeyboard.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a09ab-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a09ab-114">Error codes</span></span>



| <span data-ttu-id="a09ab-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a09ab-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a09ab-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a09ab-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a09ab-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a09ab-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a09ab-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a09ab-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a09ab-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a09ab-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a09ab-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a09ab-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a09ab-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="a09ab-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a09ab-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a09ab-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a09ab-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a09ab-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a09ab-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a09ab-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a09ab-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a09ab-125">Requirements</span></span>



| <span data-ttu-id="a09ab-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a09ab-126">Requirement</span></span> | <span data-ttu-id="a09ab-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a09ab-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09ab-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a09ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a09ab-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a09ab-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a09ab-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a09ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a09ab-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a09ab-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a09ab-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a09ab-132">End of client support</span></span><br/>    | <span data-ttu-id="a09ab-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a09ab-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a09ab-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="a09ab-134">Product</span></span><br/>                  | <span data-ttu-id="a09ab-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a09ab-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a09ab-136">Header</span><span class="sxs-lookup"><span data-stu-id="a09ab-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a09ab-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a09ab-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a09ab-138">IID</span><span class="sxs-lookup"><span data-stu-id="a09ab-138">IID</span></span><br/>                      | <span data-ttu-id="a09ab-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="a09ab-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a09ab-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a09ab-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09ab-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="a09ab-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

