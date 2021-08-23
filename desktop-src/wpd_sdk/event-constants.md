---
description: Windows Portable Geräte definieren die folgenden Ereigniswerte.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Ereigniskonstanten (PortableDevice.h)
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
ms.openlocfilehash: 5ae8a0a519af32a68bd65241f847cadcaa3d623be932a747e21a3b86338d680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704790"
---
# <a name="event-constants-portabledeviceh"></a>Ereigniskonstanten (PortableDevice.h)

Windows Portable Geräte definieren die folgenden Ereigniswerte.



| Konstante                                                                                                                                                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_WPD-EREIGNISGERÄTEFUNKTIONEN \_ \_ \_ AKTUALISIERT**</dt> </dl> | Dieses Ereignis gibt an, dass sich die Gerätefunktionen geändert haben. Clients sollten das Gerät erneut abfragen, wenn sie Basierend auf den Gerätefunktionen Entscheidungen getroffen haben.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_WPD-EREIGNISGERÄT \_ \_ ENTFERNT**</dt> </dl>                                         | Dieses Ereignis wird gesendet, wenn ein Treiber für ein Gerät entladen wird. In der Regel ist dies das Ergebnis des Trennens des Geräts.<br/> Clients sollten die **IPortableDevice-Schnittstelle** und alle [**IPortableDeviceService-Schnittstellen**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) freigeben, die in **WPD \_ EVENT PARAMETER \_ \_ PNP \_ DEVICE \_ ID** angegeben sind.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**\_ \_ \_ WPD-EREIGNISGERÄTERÜCKSETZUNG**</dt> </dl>                                               | Dieses Ereignis gibt an, dass das Gerät zurückgesetzt werden soll, und alle verbundenen Clients sollten ihre Verbindungen mit dem Gerät schließen.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_WPD-EREIGNISOBJEKT \_ \_ HINZUGEFÜGT**</dt> </dl>                                               | Dieses Ereignis gibt an, dass ein neues -Objekt auf dem Gerät verfügbar ist.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_WPD-EREIGNISOBJEKT \_ \_ ENTFERNT**</dt> </dl>                                         | Dieses Ereignis wird gesendet, nachdem ein zuvor vorhandenes -Objekt vom Gerät entfernt wurde.<br/> Das Objekt kann ein Inhaltsobjekt sein, z. B. wurde eine Bilddatei gelöscht. oder es kann sich um ein funktionales Objekt handelt, z. B. wurde ein neues Speichergerät vom Gerät entfernt.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**\_WPD-EREIGNISOBJEKTÜBERTRAGUNG \_ \_ \_ ANGEFORDERT**</dt> </dl>       | Dieses Ereignis wird gesendet, um eine Anwendung anzufordern, ein bestimmtes Objekt vom Gerät zu übertragen.<br/> Das -Objekt ist in der Regel ein Inhaltsobjekt, z. B. eine Bilddatei.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_WPD-EREIGNISOBJEKT \_ \_ AKTUALISIERT**</dt> </dl>                                         | Dieses Ereignis wird gesendet, nachdem ein Objekt aktualisiert wurde, und jeder verbundene Client sollte seine Ansicht dieses Objekts aktualisieren.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_WPD-EREIGNISDIENSTMETHODE \_ \_ \_ ABGESCHLOSSEN**</dt> </dl>             | Dieses Ereignis wird gesendet, wenn ein Treiber das Aufrufen einer Dienstmethode abgeschlossen hat. Dieses Ereignis muss auch dann gesendet werden, wenn die Methode fehlschlägt. Dies ist ein internes WPD DDI-Ereignis, das für anwendungen nicht über [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) oder [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise)verfügbar ist.<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_ \_ WPD-EREIGNISSPEICHERFORMAT \_**</dt> </dl>                                         | Dieses Ereignis gibt den Fortschritt eines Formatvorgangs für ein Speicherobjekt an.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten](constants.md)
</dt> </dl>

 

 




