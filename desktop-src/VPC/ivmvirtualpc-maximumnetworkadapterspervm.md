---
title: Ivmvirtualpc maximumnetworkadapterspervm-Eigenschaft (vpccominterfaces. h)
description: Maximale Anzahl von Netzwerkschnittstellen pro virtuellem Computer.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Maximumnetworkadapterspervm-Eigenschaft virtueller PC
- Maximumnetworkadapterspervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumnetworkadapterspervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102794"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="ba112-106">Ivmvirtualpc:: maximumnetworkadapterspervm (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba112-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="ba112-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba112-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba112-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba112-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba112-109">Hiermit wird die maximale Anzahl von Netzwerkschnittstellen pro virtuellem Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba112-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="ba112-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ba112-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba112-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba112-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="ba112-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ba112-112">Property value</span></span>

<span data-ttu-id="ba112-113">Die maximale Anzahl von Netzwerkschnittstellen pro virtuellem Computer.</span><span class="sxs-lookup"><span data-stu-id="ba112-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba112-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ba112-114">Error codes</span></span>



| <span data-ttu-id="ba112-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ba112-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="ba112-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ba112-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba112-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="ba112-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba112-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ba112-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="ba112-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ba112-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ba112-121"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="ba112-122">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="ba112-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ba112-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba112-123">Requirements</span></span>



| <span data-ttu-id="ba112-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba112-124">Requirement</span></span> | <span data-ttu-id="ba112-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ba112-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba112-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba112-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba112-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba112-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba112-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba112-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba112-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ba112-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba112-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ba112-130">End of client support</span></span><br/>    | <span data-ttu-id="ba112-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba112-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba112-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="ba112-132">Product</span></span><br/>                  | <span data-ttu-id="ba112-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba112-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba112-134">Header</span><span class="sxs-lookup"><span data-stu-id="ba112-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba112-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ba112-136">IID</span><span class="sxs-lookup"><span data-stu-id="ba112-136">IID</span></span><br/>                      | <span data-ttu-id="ba112-137">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="ba112-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ba112-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba112-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba112-139">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="ba112-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

