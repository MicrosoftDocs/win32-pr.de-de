---
title: Ivmnetworkadapter-virtualmachine-Eigenschaft (vpccominterfaces. h)
description: Ruft den virtuellen Computer ab, der dieser Netzwerkschnittstelle zugeordnet ist.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- Virtualmachine-Eigenschaft virtueller PC
- Virtualmachine-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, virtualmachine (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040047"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="da0f6-106">Ivmnetworkadapter:: virtualmachine-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="da0f6-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="da0f6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="da0f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="da0f6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da0f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="da0f6-109">Ruft den virtuellen Computer ab, der dieser Netzwerkschnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="da0f6-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="da0f6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="da0f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0f6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="da0f6-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="da0f6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="da0f6-112">Property value</span></span>

<span data-ttu-id="da0f6-113">Eine [**ivmvirtualmachine**](ivmvirtualmachine.md) -Schnittstelle, die den virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="da0f6-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="da0f6-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="da0f6-114">Error codes</span></span>



| <span data-ttu-id="da0f6-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="da0f6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="da0f6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="da0f6-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="da0f6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da0f6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="da0f6-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="da0f6-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="da0f6-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="da0f6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="da0f6-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="da0f6-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="da0f6-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="da0f6-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="da0f6-122">Der virtuelle Computer kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="da0f6-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="da0f6-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="da0f6-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="da0f6-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="da0f6-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="da0f6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da0f6-125">Requirements</span></span>



| <span data-ttu-id="da0f6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da0f6-126">Requirement</span></span> | <span data-ttu-id="da0f6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="da0f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da0f6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da0f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da0f6-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da0f6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da0f6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da0f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da0f6-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="da0f6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="da0f6-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="da0f6-132">End of client support</span></span><br/>    | <span data-ttu-id="da0f6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da0f6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="da0f6-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="da0f6-134">Product</span></span><br/>                  | <span data-ttu-id="da0f6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="da0f6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="da0f6-136">Header</span><span class="sxs-lookup"><span data-stu-id="da0f6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="da0f6-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0f6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="da0f6-138">IID</span><span class="sxs-lookup"><span data-stu-id="da0f6-138">IID</span></span><br/>                      | <span data-ttu-id="da0f6-139">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="da0f6-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="da0f6-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da0f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0f6-141">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="da0f6-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

