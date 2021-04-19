---
title: Ivmvirtualnetwork Network Adapters-Eigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von NICs ab, die an das virtuelle Netzwerk angefügt sind.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- NetworkAdapters-Eigenschaft virtueller PC
- NetworkAdapters-Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Netzwerkadaptern (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339594"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a><span data-ttu-id="b803b-106">Ivmvirtualnetwork:: NetworkAdapters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b803b-106">IVMVirtualNetwork::NetworkAdapters property</span></span>

<span data-ttu-id="b803b-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b803b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b803b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b803b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b803b-109">Ruft eine Aufzähl Bare Auflistung von NICs ab, die an das virtuelle Netzwerk angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="b803b-109">Retrieves an enumerable collection of NICs attached to the virtual network.</span></span>

<span data-ttu-id="b803b-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b803b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b803b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b803b-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="b803b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b803b-112">Property value</span></span>

<span data-ttu-id="b803b-113">Eine neue [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) , die die virtuellen NICs enthält, die mit diesem virtuellen Netzwerk verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="b803b-113">A new [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) which holds the virtual NICs attached to this virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b803b-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b803b-114">Error codes</span></span>



| <span data-ttu-id="b803b-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="b803b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b803b-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b803b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b803b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b803b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b803b-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b803b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b803b-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b803b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b803b-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b803b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b803b-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b803b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b803b-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b803b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b803b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b803b-123">Requirements</span></span>



| <span data-ttu-id="b803b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b803b-124">Requirement</span></span> | <span data-ttu-id="b803b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b803b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b803b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b803b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b803b-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b803b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b803b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b803b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b803b-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b803b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b803b-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b803b-130">End of client support</span></span><br/>    | <span data-ttu-id="b803b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b803b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b803b-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="b803b-132">Product</span></span><br/>                  | <span data-ttu-id="b803b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b803b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b803b-134">Header</span><span class="sxs-lookup"><span data-stu-id="b803b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b803b-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b803b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b803b-136">IID</span><span class="sxs-lookup"><span data-stu-id="b803b-136">IID</span></span><br/>                      | <span data-ttu-id="b803b-137">IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.</span><span class="sxs-lookup"><span data-stu-id="b803b-137">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b803b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b803b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b803b-139">**Ivmvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="b803b-139">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

