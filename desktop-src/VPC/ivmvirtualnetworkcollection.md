---
title: Ivmvirtualnetworkcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Auflistung von ivmvirtualnetwork-Objekten. Verwenden Sie zum Abrufen eines ivmvirtualnetworkcollection-Objekts die ivmvirtualpc-virtualnetworks-Eigenschaft.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Ivmvirtualnetworkcollection-Schnittstelle virtueller PC
- Ivmvirtualnetworkcollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743081"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="0a82a-106">Ivmvirtualnetworkcollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0a82a-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="0a82a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a82a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0a82a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0a82a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0a82a-109">Definiert eine Auflistung von [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="0a82a-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="0a82a-110">Zum Abrufen eines **ivmvirtualnetworkcollection** -Objekts verwenden Sie die [**ivmvirtualpc:: virtualnetworks**](ivmvirtualpc-virtualnetworks.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0a82a-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="0a82a-111">Member</span><span class="sxs-lookup"><span data-stu-id="0a82a-111">Members</span></span>

<span data-ttu-id="0a82a-112">Die **ivmvirtualnetworkcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0a82a-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0a82a-113">**Ivmvirtualnetworkcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0a82a-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="0a82a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a82a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a82a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a82a-115">Properties</span></span>

<span data-ttu-id="0a82a-116">Die **ivmvirtualnetworkcollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a82a-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="0a82a-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0a82a-117">Property</span></span>                                                             | <span data-ttu-id="0a82a-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="0a82a-118">Access type</span></span>          | <span data-ttu-id="0a82a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a82a-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a82a-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="0a82a-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="0a82a-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a82a-121">Read-only</span></span><br/> | <span data-ttu-id="0a82a-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0a82a-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="0a82a-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="0a82a-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="0a82a-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a82a-124">Read-only</span></span><br/> | <span data-ttu-id="0a82a-125">Die Anzahl der virtuellen Netzwerke in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0a82a-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="0a82a-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a82a-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="0a82a-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0a82a-127">Read-only</span></span><br/> | <span data-ttu-id="0a82a-128">Das [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="0a82a-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a82a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a82a-129">Requirements</span></span>



| <span data-ttu-id="0a82a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a82a-130">Requirement</span></span> | <span data-ttu-id="0a82a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="0a82a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a82a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a82a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0a82a-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a82a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a82a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a82a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0a82a-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0a82a-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0a82a-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0a82a-136">End of client support</span></span><br/>    | <span data-ttu-id="0a82a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a82a-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="0a82a-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="0a82a-138">Product</span></span><br/>                  | <span data-ttu-id="0a82a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0a82a-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="0a82a-140">Header</span><span class="sxs-lookup"><span data-stu-id="0a82a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a82a-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a82a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="0a82a-142">IID</span><span class="sxs-lookup"><span data-stu-id="0a82a-142">IID</span></span><br/>                      | <span data-ttu-id="0a82a-143">IID \_ ivmvirtualnetworkcollection ist als 8ed680be-4242-4b2a-A21C-1982d8b0f. definiert.</span><span class="sxs-lookup"><span data-stu-id="0a82a-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

