---
description: Unterstützt die Enumeration von iportabledeviceconnector-Schnittstellen, die MTP/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Ienumportabledeviceconnectors-Schnittstelle (devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216071"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="d071f-103">Ienumportabledebug Controller-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d071f-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="d071f-104">Die **ienumportabledeviceconnectors** -Schnittstelle unterstützt die Enumeration von [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Schnittstellen, die MTP/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden.</span><span class="sxs-lookup"><span data-stu-id="d071f-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="d071f-105">Beachten Sie, dass dadurch alle zuvor gekoppelten Geräte abgerufen werden, einschließlich Geräte, die gekoppelt, aber nicht getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="d071f-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="d071f-106">Um festzustellen, ob ein Gerät weiterhin verbunden ist, Fragen Sie die **devpkey-Eigenschaft \_ mtpbth \_ IsConnected** für dieses Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="d071f-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="d071f-107">Member</span><span class="sxs-lookup"><span data-stu-id="d071f-107">Members</span></span>

<span data-ttu-id="d071f-108">Die **ienumportabledebug Controller** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d071f-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d071f-109">**Ienumportabletoviceconnectors** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d071f-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="d071f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d071f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d071f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d071f-111">Methods</span></span>

<span data-ttu-id="d071f-112">Die **ienumportabledeviceconnectors** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d071f-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="d071f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d071f-113">Method</span></span>                                               | <span data-ttu-id="d071f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d071f-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d071f-115">**Klon**</span><span class="sxs-lookup"><span data-stu-id="d071f-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="d071f-116">Erstellt eine Kopie der aktuellen **ienumportabledebug Controller** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d071f-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="d071f-117">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="d071f-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="d071f-118">Ruft das nächste oder mehrere [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekte in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="d071f-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="d071f-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="d071f-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="d071f-120">Setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="d071f-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="d071f-121">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="d071f-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="d071f-122">Überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="d071f-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="d071f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d071f-123">Requirements</span></span>



| <span data-ttu-id="d071f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d071f-124">Requirement</span></span> | <span data-ttu-id="d071f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d071f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d071f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d071f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d071f-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d071f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="d071f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d071f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d071f-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d071f-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="d071f-130">Header</span><span class="sxs-lookup"><span data-stu-id="d071f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d071f-131"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d071f-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="d071f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="d071f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d071f-133"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d071f-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="d071f-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d071f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d071f-135"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d071f-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

