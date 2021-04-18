---
title: Ivmnetworkadapter-Schnittstelle (vpccominterfaces. h)
description: Dient als Schnittstelle für eine virtuelle Netzwerkschnittstellenkarte.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Ivmnetworkadapter Interface Virtual PC
- Virtueller Computer für ivmnetworkadapter Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391957"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="f6eed-105">Ivmnetworkadapter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6eed-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="f6eed-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6eed-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f6eed-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f6eed-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f6eed-108">Dient als Schnittstelle für eine virtuelle Netzwerkschnittstellenkarte (NIC).</span><span class="sxs-lookup"><span data-stu-id="f6eed-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="f6eed-109">Es wird verwendet, um einzurichten, wie ein virtueller Computer vernetzt ist.</span><span class="sxs-lookup"><span data-stu-id="f6eed-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="f6eed-110">Netzwerkschnittstellenkarten können mithilfe von [**ivmvirtualmachine:: addnetworkadapter**](ivmvirtualmachine-addnetworkadapter.md) und [**ivmvirtualmachine:: removenetworkadapter**](ivmvirtualmachine-removenetworkadapter.md)hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f6eed-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="f6eed-111">Sie können auch ein **ivmnetworkadapter** -Objekt aus der [**ivmnetworkadaptercollection**](ivmnetworkadaptercollection.md) -Sammlung abrufen, die von den Eigenschaften [**ivmvirtualmachine:: NetworkAdapters**](ivmvirtualmachine-networkadapters.md) oder [**ivmvirtualnetwork:: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f6eed-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="f6eed-112">Member</span><span class="sxs-lookup"><span data-stu-id="f6eed-112">Members</span></span>

<span data-ttu-id="f6eed-113">Die **ivmnetworkadapter** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f6eed-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f6eed-114">**Ivmnetworkadapter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f6eed-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="f6eed-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6eed-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6eed-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6eed-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6eed-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="f6eed-117">Methods</span></span>

<span data-ttu-id="f6eed-118">Die **ivmnetworkadapter** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f6eed-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="f6eed-119">Methode</span><span class="sxs-lookup"><span data-stu-id="f6eed-119">Method</span></span>                                                                         | <span data-ttu-id="f6eed-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6eed-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="f6eed-121">**\_id**</span><span class="sxs-lookup"><span data-stu-id="f6eed-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="f6eed-122">Ruft den internen Bezeichner dieser Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="f6eed-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="f6eed-123">**Attachanvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="f6eed-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="f6eed-124">Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="f6eed-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="f6eed-125">**Detachfromvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="f6eed-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="f6eed-126">Trennt die Netzwerkschnittstelle von Ihrem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f6eed-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="f6eed-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f6eed-127">Properties</span></span>

<span data-ttu-id="f6eed-128">Die **ivmnetworkadapter** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6eed-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="f6eed-129">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6eed-129">Property</span></span>                                                                                  | <span data-ttu-id="f6eed-130">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f6eed-130">Access type</span></span>           | <span data-ttu-id="f6eed-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6eed-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="f6eed-132">**Ethernetaddress**</span><span class="sxs-lookup"><span data-stu-id="f6eed-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="f6eed-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6eed-133">Read/write</span></span><br/> | <span data-ttu-id="f6eed-134">Die Ethernet-Adresse (Mac-Adresse) der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f6eed-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="f6eed-135">**Isethernetaddressdynamic**</span><span class="sxs-lookup"><span data-stu-id="f6eed-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="f6eed-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f6eed-136">Read/write</span></span><br/> | <span data-ttu-id="f6eed-137">Gibt an, ob die Ethernet-Adresse dynamisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f6eed-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="f6eed-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f6eed-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="f6eed-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6eed-139">Read-only</span></span><br/>  | <span data-ttu-id="f6eed-140">Der virtuelle Computer, der dieser Netzwerkschnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f6eed-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="f6eed-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="f6eed-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="f6eed-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f6eed-142">Read-only</span></span><br/>  | <span data-ttu-id="f6eed-143">Das virtuelle Netzwerk, an das die Netzwerkschnittstelle angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f6eed-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="f6eed-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6eed-144">Remarks</span></span>

<span data-ttu-id="f6eed-145">Die standardethernet-Adresse für eine Netzwerkschnittstelle ist "00-00-00-00-00-00", die von den meisten Betriebssystemen als ungültige Ethernet-Adresse angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="f6eed-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="f6eed-146">Wenn [**isethernetaddressdynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) auf **false** festgelegt ist, muss [**ethernetaddress**](ivmnetworkadapter-ethernetaddress.md) mit einer gültigen Ethernet-Netzwerkadresse initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6eed-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="f6eed-147">In den folgenden Prozeduren wird erläutert, wie die **ivmnetworkadapter** -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6eed-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="f6eed-148">**So fügen Sie eine virtuelle NIC an eine Host-NIC an**</span><span class="sxs-lookup"><span data-stu-id="f6eed-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="f6eed-149">Virtuelle (Guest) NICs sind nicht direkt an eine Host-NIC angefügt.</span><span class="sxs-lookup"><span data-stu-id="f6eed-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="f6eed-150">Stattdessen wird die virtuelle NIC an ein virtuelles Netzwerk angefügt, das mit einer Host-NIC verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f6eed-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="f6eed-151">Weitere Informationen zum Konfigurieren virtueller Netzwerke finden Sie unter [**ivmvirtualnetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="f6eed-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="f6eed-152">Verwenden Sie die [**attachdevirtualnetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) -Methode, um die virtuelle NIC an ein virtuelles Netzwerk anzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6eed-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="f6eed-153">**So trennen Sie eine virtuelle NIC vom virtuellen Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="f6eed-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="f6eed-154">Die Methode [**detachfromvirtualnetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) trennt die virtuelle NIC vom virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f6eed-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="f6eed-155">Nachdem diese Funktion aufgerufen wurde, gibt die [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) -Eigenschaft eine ungültige virtuelle Netzwerk-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="f6eed-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="f6eed-156">**So entfernen Sie eine virtuelle NIC aus einer virtuellen Maschine, wenn Sie über das virtuelle NIC-Objekt verfügen**</span><span class="sxs-lookup"><span data-stu-id="f6eed-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="f6eed-157">Holen Sie den virtuellen Computer, der der virtuellen NIC zugeordnet ist, mithilfe der [**virtualmachine**](ivmnetworkadapter-virtualmachine.md) -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="f6eed-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="f6eed-158">Verwenden Sie das aktuelle-Objekt als Parameter für die [**ivmvirtualmachine:: removenetworkadapter**](ivmvirtualmachine-removenetworkadapter.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f6eed-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6eed-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6eed-159">Requirements</span></span>



| <span data-ttu-id="f6eed-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6eed-160">Requirement</span></span> | <span data-ttu-id="f6eed-161">Wert</span><span class="sxs-lookup"><span data-stu-id="f6eed-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6eed-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6eed-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f6eed-163">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6eed-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6eed-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6eed-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f6eed-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6eed-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f6eed-166">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f6eed-166">End of client support</span></span><br/>    | <span data-ttu-id="f6eed-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6eed-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f6eed-168">Produkt</span><span class="sxs-lookup"><span data-stu-id="f6eed-168">Product</span></span><br/>                  | <span data-ttu-id="f6eed-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f6eed-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f6eed-170">Header</span><span class="sxs-lookup"><span data-stu-id="f6eed-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6eed-171"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6eed-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f6eed-172">IID</span><span class="sxs-lookup"><span data-stu-id="f6eed-172">IID</span></span><br/>                      | <span data-ttu-id="f6eed-173">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="f6eed-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

