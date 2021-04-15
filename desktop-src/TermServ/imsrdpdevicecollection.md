---
title: Imsrdpdebug-Schnittstelle
description: Stellt eine Auflistung von Geräte Objekten dar.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Imsrdpentvicecollection-Schnittstelle Remotedesktopdienste
- Imsrdpdebug-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391524"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="afa59-105">Imsrdpdebug-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="afa59-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="afa59-106">Stellt eine Auflistung von Geräte Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="afa59-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="afa59-107">Member</span><span class="sxs-lookup"><span data-stu-id="afa59-107">Members</span></span>

<span data-ttu-id="afa59-108">Die **imsrdpdebug** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="afa59-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="afa59-109">**Imsrdptovicecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="afa59-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="afa59-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="afa59-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="afa59-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afa59-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="afa59-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="afa59-112">Methods</span></span>

<span data-ttu-id="afa59-113">Die **imsrdpdevicecollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="afa59-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="afa59-114">Methode</span><span class="sxs-lookup"><span data-stu-id="afa59-114">Method</span></span>                                                        | <span data-ttu-id="afa59-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afa59-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="afa59-116">**Redevices**</span><span class="sxs-lookup"><span data-stu-id="afa59-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="afa59-117">Aktualisiert die Liste der-Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="afa59-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="afa59-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afa59-118">Properties</span></span>

<span data-ttu-id="afa59-119">Die **imsrdpentvicecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="afa59-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="afa59-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="afa59-120">Property</span></span>                                                                 | <span data-ttu-id="afa59-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="afa59-121">Access type</span></span>          | <span data-ttu-id="afa59-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afa59-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="afa59-123">**Devicebyid**</span><span class="sxs-lookup"><span data-stu-id="afa59-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="afa59-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afa59-124">Read-only</span></span><br/> | <span data-ttu-id="afa59-125">Ruft das Gerät mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="afa59-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="afa59-126">**Devicebyindex**</span><span class="sxs-lookup"><span data-stu-id="afa59-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="afa59-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afa59-127">Read-only</span></span><br/> | <span data-ttu-id="afa59-128">Ruft das Gerät am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="afa59-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="afa59-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="afa59-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="afa59-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="afa59-130">Read-only</span></span><br/> | <span data-ttu-id="afa59-131">Ruft die Anzahl der-Objekte in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="afa59-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="afa59-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afa59-132">Requirements</span></span>



| <span data-ttu-id="afa59-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afa59-133">Requirement</span></span> | <span data-ttu-id="afa59-134">Wert</span><span class="sxs-lookup"><span data-stu-id="afa59-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="afa59-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afa59-135">Minimum supported client</span></span><br/> | <span data-ttu-id="afa59-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afa59-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="afa59-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afa59-137">Minimum supported server</span></span><br/> | <span data-ttu-id="afa59-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afa59-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="afa59-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="afa59-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="afa59-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afa59-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="afa59-141">DLL</span><span class="sxs-lookup"><span data-stu-id="afa59-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afa59-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afa59-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="afa59-143">IID</span><span class="sxs-lookup"><span data-stu-id="afa59-143">IID</span></span><br/>                      | <span data-ttu-id="afa59-144">IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.</span><span class="sxs-lookup"><span data-stu-id="afa59-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afa59-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afa59-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa59-146">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="afa59-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="afa59-147">**Imsrdpdevice**</span><span class="sxs-lookup"><span data-stu-id="afa59-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

