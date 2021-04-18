---
title: Imsrdpdevice-Schnittstelle
description: Enthält Informationen zu einem Geräte Objekt.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Imsrdpdevice-Schnittstelle Remotedesktopdienste
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337914"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="7a12b-105">Imsrdpdevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7a12b-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="7a12b-106">Enthält Informationen zu einem Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a12b-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="7a12b-107">Member</span><span class="sxs-lookup"><span data-stu-id="7a12b-107">Members</span></span>

<span data-ttu-id="7a12b-108">Die **imsrdpdevice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7a12b-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7a12b-109">**Imsrdpdevice** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7a12b-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7a12b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a12b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a12b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a12b-111">Properties</span></span>

<span data-ttu-id="7a12b-112">Die **imsrdpdevice** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a12b-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="7a12b-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7a12b-113">Property</span></span>                                                               | <span data-ttu-id="7a12b-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7a12b-114">Access type</span></span>           | <span data-ttu-id="7a12b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a12b-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a12b-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="7a12b-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="7a12b-117">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a12b-117">Read-only</span></span><br/>  | <span data-ttu-id="7a12b-118">Ruft die Geräte Beschreibung ab, die dem Benutzer angezeigt werden soll, wenn der Anzeige Name nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7a12b-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="7a12b-119">**Geräte-ID**</span><span class="sxs-lookup"><span data-stu-id="7a12b-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="7a12b-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a12b-120">Read-only</span></span><br/>  | <span data-ttu-id="7a12b-121">Ruft den geräteinstanzbezeichner des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="7a12b-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="7a12b-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="7a12b-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="7a12b-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a12b-123">Read-only</span></span><br/>  | <span data-ttu-id="7a12b-124">Ruft den anzeigen Amen für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="7a12b-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="7a12b-125">**Redirectionstate**</span><span class="sxs-lookup"><span data-stu-id="7a12b-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="7a12b-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a12b-126">Read/write</span></span><br/> | <span data-ttu-id="7a12b-127">Gibt den Umleitungs Status des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="7a12b-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="7a12b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a12b-128">Requirements</span></span>



| <span data-ttu-id="7a12b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a12b-129">Requirement</span></span> | <span data-ttu-id="7a12b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7a12b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a12b-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a12b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7a12b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a12b-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7a12b-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a12b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7a12b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a12b-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7a12b-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7a12b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a12b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a12b-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a12b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7a12b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a12b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a12b-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a12b-139">IID</span><span class="sxs-lookup"><span data-stu-id="7a12b-139">IID</span></span><br/>                      | <span data-ttu-id="7a12b-140">IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.</span><span class="sxs-lookup"><span data-stu-id="7a12b-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7a12b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a12b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a12b-142">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="7a12b-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="7a12b-143">**Imsrdpde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="7a12b-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

