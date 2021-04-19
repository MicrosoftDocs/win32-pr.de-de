---
description: Die Geräteschnittstelle kann durch einen GUID-Wert beschrieben werden. Tragbare Windows-Geräte definieren die folgende Geräteschnittstelle.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: Geräteschnittstellen-GUIDs (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370133"
---
# <a name="device-interface-guids"></a><span data-ttu-id="48f38-104">Geräteschnittstellen-GUIDs</span><span class="sxs-lookup"><span data-stu-id="48f38-104">Device Interface GUIDs</span></span>

<span data-ttu-id="48f38-105">Die Geräteschnittstelle kann durch einen **GUID** -Wert beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="48f38-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="48f38-106">Tragbare Windows-Geräte definieren die folgende Geräteschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="48f38-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="48f38-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="48f38-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="48f38-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48f38-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="48f38-109"><dt>**GUID- \_ devinterface- \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="48f38-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="48f38-110">Identifiziert Geräte, die in einer normalen WPD-Enumeration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="48f38-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="48f38-111">Alle Geräte, die diese Schnittstellen-GUID registrieren, werden aufgezählt, wenn eine Anwendung die [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="48f38-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="48f38-112"><dt>**GUID \_ devinterface- \_ WPD \_ Privat**</dt></span><span class="sxs-lookup"><span data-stu-id="48f38-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="48f38-113">Identifiziert Geräte, die während einer normalen WPD-Enumeration nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="48f38-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="48f38-114">Alle Geräte, die diese Schnittstellen-GUID registrieren, werden nur aufgelistet, wenn eine Anwendung die [**iportabledevicemanager:: getprivatedevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="48f38-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="48f38-115"><dt>**GUID- \_ devinterface- \_ WPD- \_ Dienst**</dt></span><span class="sxs-lookup"><span data-stu-id="48f38-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="48f38-116">In Windows 7 können Anwendungen alle WPD-Geräte Dienste auflisten, indem Sie [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) aufrufen und diese Schnittstellen Klasse als Diensttyp-GUID verwenden.</span><span class="sxs-lookup"><span data-stu-id="48f38-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="48f38-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48f38-117">Requirements</span></span>



| <span data-ttu-id="48f38-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48f38-118">Requirement</span></span> | <span data-ttu-id="48f38-119">Wert</span><span class="sxs-lookup"><span data-stu-id="48f38-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f38-120">Header</span><span class="sxs-lookup"><span data-stu-id="48f38-120">Header</span></span><br/> | <dl> <span data-ttu-id="48f38-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f38-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f38-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48f38-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f38-123">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="48f38-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




