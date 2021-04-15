---
title: Ivmvirtualmachine Network Adapters-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von NICs ab, die an den virtuellen Computer angefügt sind.
ms.assetid: 3877edf7-92b8-43c9-8229-a198a07079a4
keywords:
- NetworkAdapters-Eigenschaft virtueller PC
- NetworkAdapters-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Network Adapters (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.NetworkAdapters
- IVMVirtualMachine.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ce6e1fa22eca40c037eebb48803fe182810c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391981"
---
# <a name="ivmvirtualmachinenetworkadapters-property"></a><span data-ttu-id="c8ead-106">Ivmvirtualmachine:: NetworkAdapters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c8ead-106">IVMVirtualMachine::NetworkAdapters property</span></span>

<span data-ttu-id="c8ead-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8ead-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8ead-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8ead-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8ead-109">Ruft eine Aufzähl Bare Auflistung von NICs ab, die an den virtuellen Computer angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="c8ead-109">Retrieves an enumerable collection of NICs attached to the virtual machine.</span></span>

<span data-ttu-id="c8ead-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8ead-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ead-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8ead-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c8ead-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c8ead-112">Property value</span></span>

<span data-ttu-id="c8ead-113">Ein [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c8ead-113">An [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8ead-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8ead-114">Error codes</span></span>



| <span data-ttu-id="c8ead-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c8ead-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c8ead-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c8ead-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8ead-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8ead-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c8ead-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8ead-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c8ead-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8ead-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c8ead-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c8ead-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c8ead-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c8ead-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c8ead-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c8ead-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c8ead-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8ead-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c8ead-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c8ead-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8ead-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ead-125">Requirements</span></span>



| <span data-ttu-id="c8ead-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ead-126">Requirement</span></span> | <span data-ttu-id="c8ead-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ead-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ead-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ead-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ead-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8ead-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8ead-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8ead-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ead-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8ead-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8ead-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ead-132">End of client support</span></span><br/>    | <span data-ttu-id="c8ead-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8ead-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8ead-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="c8ead-134">Product</span></span><br/>                  | <span data-ttu-id="c8ead-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8ead-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8ead-136">Header</span><span class="sxs-lookup"><span data-stu-id="c8ead-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ead-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ead-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8ead-138">IID</span><span class="sxs-lookup"><span data-stu-id="c8ead-138">IID</span></span><br/>                      | <span data-ttu-id="c8ead-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="c8ead-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c8ead-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ead-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ead-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="c8ead-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

