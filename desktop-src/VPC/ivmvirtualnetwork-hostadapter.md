---
title: Ivmvirtualnetwork-hostanapter-Eigenschaft (vpccominterfaces. h)
description: Der Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Host Host Eigenschaft Virtual PC
- Host Host Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Host-apter (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040865"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="cc235-106">Ivmvirtualnetwork:: hostapter (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc235-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="cc235-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc235-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cc235-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cc235-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cc235-109">Ruft den Namen des Adapters ab, mit dem das virtuelle Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cc235-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="cc235-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cc235-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc235-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc235-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="cc235-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cc235-112">Property value</span></span>

<span data-ttu-id="cc235-113">Der Name des Host Adapters, mit dem das virtuelle Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cc235-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cc235-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cc235-114">Error codes</span></span>



| <span data-ttu-id="cc235-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="cc235-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="cc235-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cc235-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc235-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cc235-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="cc235-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc235-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="cc235-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cc235-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="cc235-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="cc235-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="cc235-121"><dt>VM \_ E- \_ Adapter \_ nicht \_ gefunden</dt> <dt>0xa0040700</dt></span><span class="sxs-lookup"><span data-stu-id="cc235-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="cc235-122">Der Host-Ethernet-Adapter, mit dem dieses virtuelle Netzwerk verbunden war, ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc235-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="cc235-123">Der hostethernet-Adapter wurde möglicherweise entfernt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cc235-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="cc235-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cc235-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="cc235-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cc235-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="cc235-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc235-126">Remarks</span></span>

<span data-ttu-id="cc235-127">Mit dem virtuellen Netzwerkadapter kann ein virtuelles Netzwerk mit externen Netzwerken kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cc235-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="cc235-128">Normalerweise ist ein Adapter pro Ethernet-Adapter auf dem Host Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="cc235-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="cc235-129">Nehmen wir beispielsweise an, dass ein Host Computer über einen Adapter mit der Bezeichnung "10/100 ENET" verfügt.</span><span class="sxs-lookup"><span data-stu-id="cc235-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="cc235-130">Wenn Sie eine virtuelle NIC mit dem Netzwerk verbinden möchten, das mit "10/100 ENET" verbunden ist, legen Sie **die Eigenschaft "** Network Host" des virtuellen Netzwerks auf "10/100 ENET" fest, und verbinden Sie die virtuelle NIC mit diesem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cc235-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="cc235-131">Wenn die **Hostadapter** -Eigenschaft auf eine leere Zeichenfolge ("") festgelegt ist, wird der virtuelle NIC-Adapter mit dem Netzwerk "Internal Network" oder "Shared Networking (NAT)" verbunden.</span><span class="sxs-lookup"><span data-stu-id="cc235-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="cc235-132">Virtuelle NICs, die an das Netzwerk "internes Netzwerk" angefügt werden, haben keinen Zugriff auf externe Netzwerke auf dem System Host.</span><span class="sxs-lookup"><span data-stu-id="cc235-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="cc235-133">Die virtuellen NICs, die mit diesem virtuellen Netzwerk verbunden sind, können jedoch immer noch miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cc235-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="cc235-134">Auf die gesamte Liste der Adapter kann über die [**ivmhostinfo:: NetworkAdapters**](ivmhostinfo-networkadapters.md) -Eigenschaft zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cc235-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc235-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc235-135">Requirements</span></span>



| <span data-ttu-id="cc235-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc235-136">Requirement</span></span> | <span data-ttu-id="cc235-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cc235-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc235-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc235-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cc235-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc235-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc235-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc235-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cc235-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc235-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cc235-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cc235-142">End of client support</span></span><br/>    | <span data-ttu-id="cc235-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc235-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cc235-144">Produkt</span><span class="sxs-lookup"><span data-stu-id="cc235-144">Product</span></span><br/>                  | <span data-ttu-id="cc235-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cc235-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cc235-146">Header</span><span class="sxs-lookup"><span data-stu-id="cc235-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc235-147"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc235-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cc235-148">IID</span><span class="sxs-lookup"><span data-stu-id="cc235-148">IID</span></span><br/>                      | <span data-ttu-id="cc235-149">IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.</span><span class="sxs-lookup"><span data-stu-id="cc235-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cc235-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc235-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc235-151">**Ivmvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="cc235-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

