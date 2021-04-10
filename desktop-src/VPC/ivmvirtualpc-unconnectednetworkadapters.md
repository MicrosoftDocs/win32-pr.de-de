---
title: Ivmvirtualpc unconnectednetworkadapters-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von nicht verbundenen Netzwerkschnittstellen ab.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- Unconnectednetworkadapters-Eigenschaft virtueller PC
- Unconnectednetworkadapters-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, unconnectednetworkadapters (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040734"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a><span data-ttu-id="f96a6-106">Ivmvirtualpc:: unconnectednetworkadapters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f96a6-106">IVMVirtualPC::UnconnectedNetworkAdapters property</span></span>

<span data-ttu-id="f96a6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f96a6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f96a6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f96a6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f96a6-109">Ruft eine Aufzähl Bare Auflistung von nicht verbundenen Netzwerkschnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="f96a6-109">Retrieves an enumerable collection of unconnected network interfaces.</span></span>

<span data-ttu-id="f96a6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f96a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96a6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f96a6-111">Syntax</span></span>


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="f96a6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f96a6-112">Property value</span></span>

<span data-ttu-id="f96a6-113">Eine Auflistung von nicht verbundenen [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="f96a6-113">A collection of unconnected [**IVMNetworkAdapter**](ivmnetworkadapter.md) objects.</span></span> <span data-ttu-id="f96a6-114">Siehe [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md).</span><span class="sxs-lookup"><span data-stu-id="f96a6-114">See [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f96a6-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f96a6-115">Error codes</span></span>



| <span data-ttu-id="f96a6-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="f96a6-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f96a6-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f96a6-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f96a6-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f96a6-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f96a6-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f96a6-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f96a6-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f96a6-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f96a6-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f96a6-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f96a6-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f96a6-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f96a6-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f96a6-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f96a6-124"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f96a6-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f96a6-125">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="f96a6-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f96a6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f96a6-126">Requirements</span></span>



| <span data-ttu-id="f96a6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f96a6-127">Requirement</span></span> | <span data-ttu-id="f96a6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f96a6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96a6-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f96a6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f96a6-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f96a6-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f96a6-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f96a6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f96a6-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f96a6-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f96a6-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f96a6-133">End of client support</span></span><br/>    | <span data-ttu-id="f96a6-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f96a6-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f96a6-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="f96a6-135">Product</span></span><br/>                  | <span data-ttu-id="f96a6-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f96a6-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f96a6-137">Header</span><span class="sxs-lookup"><span data-stu-id="f96a6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f96a6-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f96a6-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f96a6-139">IID</span><span class="sxs-lookup"><span data-stu-id="f96a6-139">IID</span></span><br/>                      | <span data-ttu-id="f96a6-140">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="f96a6-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f96a6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f96a6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96a6-142">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="f96a6-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

