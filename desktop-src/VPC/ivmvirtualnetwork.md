---
title: Ivmvirtualnetwork-Schnittstelle (vpccominterfaces. h)
description: Definiert ein virtuelles Netzwerk.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Ivmvirtualnetwork Interface Virtual PC
- Ivmvirtualnetwork Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346531"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="ee027-105">Ivmvirtualnetwork-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ee027-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="ee027-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ee027-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ee027-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ee027-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ee027-108">Definiert ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ee027-108">Defines a virtual network.</span></span> <span data-ttu-id="ee027-109">**Ivmvirtualnetwork** -Objekte werden von der [**ivmvirtualpc**](ivmvirtualpc.md) -Methode " [**findvirtualnetwork**](ivmvirtualpc-findvirtualnetwork.md)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee027-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="ee027-110">Sie können auch ein **ivmvirtualnetwork** -Objekt aus dem [**ivmvirtualnetworkcollection**](ivmvirtualnetworkcollection.md) -Objekt abrufen, das von der [**ivmvirtualpc:: virtualnetworks**](ivmvirtualpc-virtualnetworks.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee027-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="ee027-111">Ein virtuelles Netzwerk besteht aus einem virtuellen Switch, der das gesamte interne Routing ausführt, und mehreren Verbindungen, die an den virtuellen Switch angeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="ee027-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="ee027-112">Dabei kann es sich um eine echte externe Host Verbindung, ein "internes Netzwerk" oder ein frei gegebenes Netzwerk (Network Network, NAT) handeln.</span><span class="sxs-lookup"><span data-stu-id="ee027-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="ee027-113">Member</span><span class="sxs-lookup"><span data-stu-id="ee027-113">Members</span></span>

<span data-ttu-id="ee027-114">Die **ivmvirtualnetwork** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ee027-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ee027-115">**Ivmvirtualnetwork** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ee027-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="ee027-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee027-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee027-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee027-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee027-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="ee027-118">Methods</span></span>

<span data-ttu-id="ee027-119">Die **ivmvirtualnetwork** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ee027-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="ee027-120">Methode</span><span class="sxs-lookup"><span data-stu-id="ee027-120">Method</span></span>                                | <span data-ttu-id="ee027-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee027-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="ee027-122">**\_id**</span><span class="sxs-lookup"><span data-stu-id="ee027-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="ee027-123">Ruft den internen Bezeichner des virtuellen Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="ee027-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ee027-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee027-124">Properties</span></span>

<span data-ttu-id="ee027-125">Die **ivmvirtualnetwork** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ee027-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="ee027-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ee027-126">Property</span></span>                                                                | <span data-ttu-id="ee027-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ee027-127">Access type</span></span>          | <span data-ttu-id="ee027-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee027-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ee027-129">**Host Adapter "**</span><span class="sxs-lookup"><span data-stu-id="ee027-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="ee027-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee027-130">Read-only</span></span><br/> | <span data-ttu-id="ee027-131">Der Name des Adapters, mit dem das virtuelle Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ee027-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="ee027-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee027-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="ee027-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee027-133">Read-only</span></span><br/> | <span data-ttu-id="ee027-134">Bestimmt, ob die virtuelle Netzwerk Instanz drahtlos ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ee027-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="ee027-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="ee027-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="ee027-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee027-136">Read-only</span></span><br/> | <span data-ttu-id="ee027-137">Der eindeutige Name der virtuellen Netzwerk Instanz.</span><span class="sxs-lookup"><span data-stu-id="ee027-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="ee027-138">**Netzwerkadapter**</span><span class="sxs-lookup"><span data-stu-id="ee027-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="ee027-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ee027-139">Read-only</span></span><br/> | <span data-ttu-id="ee027-140">Eine Aufzähl Bare Auflistung von NICs, die an das virtuelle Netzwerk angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="ee027-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="ee027-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee027-141">Requirements</span></span>



| <span data-ttu-id="ee027-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee027-142">Requirement</span></span> | <span data-ttu-id="ee027-143">Wert</span><span class="sxs-lookup"><span data-stu-id="ee027-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee027-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee027-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ee027-145">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee027-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee027-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee027-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ee027-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ee027-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ee027-148">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ee027-148">End of client support</span></span><br/>    | <span data-ttu-id="ee027-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee027-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ee027-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="ee027-150">Product</span></span><br/>                  | <span data-ttu-id="ee027-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ee027-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ee027-152">Header</span><span class="sxs-lookup"><span data-stu-id="ee027-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee027-153"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee027-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ee027-154">IID</span><span class="sxs-lookup"><span data-stu-id="ee027-154">IID</span></span><br/>                      | <span data-ttu-id="ee027-155">IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.</span><span class="sxs-lookup"><span data-stu-id="ee027-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

