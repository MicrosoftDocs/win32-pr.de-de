---
title: IMsRdpDeviceV2-Schnittstelle
description: Enthält Informationen zu einem Geräte Objekt. Dies ist eine Erweiterung der imsrdpdevice-Schnittstelle.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste
- IMsRdpDeviceV2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341773"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="80cf4-106">IMsRdpDeviceV2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="80cf4-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="80cf4-107">Enthält Informationen zu einem Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="80cf4-107">Contains information about a device object.</span></span> <span data-ttu-id="80cf4-108">Dies ist eine Erweiterung der [**imsrdpdevice**](imsrdpdevice.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="80cf4-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="80cf4-109">Member</span><span class="sxs-lookup"><span data-stu-id="80cf4-109">Members</span></span>

<span data-ttu-id="80cf4-110">Die **IMsRdpDeviceV2** -Schnittstelle erbt von [**imsrdpdevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="80cf4-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="80cf4-111">**IMsRdpDeviceV2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="80cf4-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="80cf4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80cf4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80cf4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="80cf4-113">Properties</span></span>

<span data-ttu-id="80cf4-114">Die **IMsRdpDeviceV2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80cf4-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="80cf4-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80cf4-115">Property</span></span>                                                                 | <span data-ttu-id="80cf4-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="80cf4-116">Access type</span></span>          | <span data-ttu-id="80cf4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80cf4-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80cf4-118">**Cmclassguid**</span><span class="sxs-lookup"><span data-stu-id="80cf4-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="80cf4-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-119">Read-only</span></span><br/> | <span data-ttu-id="80cf4-120">Enthält die Configuration Manager-Setup Klassen-GUID für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="80cf4-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="80cf4-121">**Cmdebug**</span><span class="sxs-lookup"><span data-stu-id="80cf4-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="80cf4-122">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-122">Read-only</span></span><br/> | <span data-ttu-id="80cf4-123">Enthält die Configuration Manager-Geräte Instanz des Geräts.</span><span class="sxs-lookup"><span data-stu-id="80cf4-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="80cf4-124">**Devicetext**</span><span class="sxs-lookup"><span data-stu-id="80cf4-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="80cf4-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-125">Read-only</span></span><br/> | <span data-ttu-id="80cf4-126">Enthält den Geräte Text.</span><span class="sxs-lookup"><span data-stu-id="80cf4-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="80cf4-127">**Driveletterbitmap**</span><span class="sxs-lookup"><span data-stu-id="80cf4-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="80cf4-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-128">Read-only</span></span><br/> | <span data-ttu-id="80cf4-129">Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="80cf4-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="80cf4-130">**Iscompositedevice**</span><span class="sxs-lookup"><span data-stu-id="80cf4-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="80cf4-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-131">Read-only</span></span><br/> | <span data-ttu-id="80cf4-132">Gibt an, ob es sich um ein zusammengesetztes Gerät handelt.</span><span class="sxs-lookup"><span data-stu-id="80cf4-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="80cf4-133">**Isoptionaldevice**</span><span class="sxs-lookup"><span data-stu-id="80cf4-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="80cf4-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-134">Read-only</span></span><br/> | <span data-ttu-id="80cf4-135">Gibt an, ob das Gerät für die USB-Umleitung optional ist.</span><span class="sxs-lookup"><span data-stu-id="80cf4-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="80cf4-136">**Isusbdevice**</span><span class="sxs-lookup"><span data-stu-id="80cf4-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="80cf4-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="80cf4-137">Read-only</span></span><br/> | <span data-ttu-id="80cf4-138">Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="80cf4-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="80cf4-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80cf4-139">Requirements</span></span>



| <span data-ttu-id="80cf4-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80cf4-140">Requirement</span></span> | <span data-ttu-id="80cf4-141">Wert</span><span class="sxs-lookup"><span data-stu-id="80cf4-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80cf4-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80cf4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="80cf4-143">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="80cf4-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="80cf4-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80cf4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="80cf4-145">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="80cf4-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="80cf4-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="80cf4-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="80cf4-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80cf4-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80cf4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="80cf4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80cf4-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80cf4-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="80cf4-150">IID</span><span class="sxs-lookup"><span data-stu-id="80cf4-150">IID</span></span><br/>                      | <span data-ttu-id="80cf4-151">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="80cf4-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





