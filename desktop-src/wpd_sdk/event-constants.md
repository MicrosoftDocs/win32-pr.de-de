---
description: Tragbare Windows-Geräte definieren die folgenden Ereignis Werte.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Ereignis Konstanten (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366719"
---
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="9d9b8-103">Ereignis Konstanten (portabledevice. h)</span><span class="sxs-lookup"><span data-stu-id="9d9b8-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="9d9b8-104">Tragbare Windows-Geräte definieren die folgenden Ereignis Werte.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="9d9b8-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="9d9b8-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="9d9b8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d9b8-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="9d9b8-107"><dt>**Gerätefunktionen für WPD- \_ Ereignisse \_ \_ \_ aktualisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="9d9b8-108">Dieses Ereignis weist darauf hin, dass sich die Gerätefunktionen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="9d9b8-109">Clients sollten das Gerät anweisen, wenn Sie auf der Grundlage der Gerätefunktionen Entscheidungen getroffen haben.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="9d9b8-110"><dt>**WPD- \_ Ereignis \_ Gerät \_ entfernt**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="9d9b8-111">Dieses Ereignis wird gesendet, wenn ein Treiber für ein Gerät entladen wird.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="9d9b8-112">In der Regel ist dies das Ergebnis des Geräts, das getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="9d9b8-113">Clients sollten die **iportabledevice** -Schnittstelle und alle [**iportabledeviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) -Schnittstellen freigeben, die im **WPD- \_ Ereignis \_ Parameter \_ PnP-Geräte- \_ \_ ID** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="9d9b8-114"><dt>**\_ \_ \_ Zurücksetzen des WPD-Ereignisses**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="9d9b8-115">Dieses Ereignis zeigt an, dass das Gerät im Begriff ist, zurückgesetzt zu werden, und alle verbundenen Clients sollten ihre Verbindungen mit dem Gerät schließen.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="9d9b8-116"><dt>**WPD- \_ Ereignis \_ Objekt \_ hinzugefügt**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="9d9b8-117">Dieses Ereignis gibt an, dass ein neues-Objekt auf dem Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="9d9b8-118"><dt>**WPD- \_ Ereignis \_ Objekt \_ entfernt**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="9d9b8-119">Dieses Ereignis wird gesendet, nachdem ein zuvor vorhandenes Objekt vom Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="9d9b8-120">Das Objekt kann z. b. ein Inhalts Objekt sein, z. b., dass eine Bilddatei gelöscht wurde. oder es kann sich um ein funktionales Objekt handeln, z. b. Wenn ein neues Speichergerät vom Gerät getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="9d9b8-121"><dt>**WPD- \_ Ereignis \_ Objekt \_ Übertragung \_ angefordert**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="9d9b8-122">Dieses Ereignis wird gesendet, um anzufordern, dass eine Anwendung ein bestimmtes Objekt vom Gerät überträgt.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="9d9b8-123">Bei dem Objekt handelt es sich in der Regel um ein Inhalts Objekt, z. b. eine Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="9d9b8-124"><dt>**WPD- \_ Ereignis \_ Objekt \_ aktualisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="9d9b8-125">Dieses Ereignis wird gesendet, nachdem ein Objekt aktualisiert wurde, und jeder verbundene Client sollte seine Ansicht des Objekts aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="9d9b8-126"><dt>**WPD- \_ Ereignis \_ Dienst Methode ist \_ \_ fertiggestellt.**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="9d9b8-127">Dieses Ereignis wird gesendet, wenn ein Treiber den Aufruf einer Dienst Methode abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="9d9b8-128">Dieses Ereignis muss gesendet werden, auch wenn die Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="9d9b8-129">Hierbei handelt es sich um ein internes WPD-DDI-Ereignis, das für keine Anwendungen über [**iportabledevice:: Rat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) oder [**iportabledebug:: Rat**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise)verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="9d9b8-130"><dt>**WPD- \_ Ereignis \_ Speicher \_ Format**</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="9d9b8-131">Dieses Ereignis gibt den Fortschritt eines Formatierungs Vorgangs für ein Speicher Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9d9b8-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="9d9b8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d9b8-132">Requirements</span></span>



| <span data-ttu-id="9d9b8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d9b8-133">Requirement</span></span> | <span data-ttu-id="9d9b8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9d9b8-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9b8-135">Header</span><span class="sxs-lookup"><span data-stu-id="9d9b8-135">Header</span></span><br/> | <dl> <span data-ttu-id="9d9b8-136"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b8-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d9b8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d9b8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d9b8-138">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9d9b8-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




