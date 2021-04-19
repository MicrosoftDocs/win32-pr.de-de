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
# <a name="event-constants-portabledeviceh"></a>Ereignis Konstanten (portabledevice. h)

Tragbare Windows-Geräte definieren die folgenden Ereignis Werte.



| Konstante                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**Gerätefunktionen für WPD- \_ Ereignisse \_ \_ \_ aktualisiert**</dt> </dl> | Dieses Ereignis weist darauf hin, dass sich die Gerätefunktionen geändert haben. Clients sollten das Gerät anweisen, wenn Sie auf der Grundlage der Gerätefunktionen Entscheidungen getroffen haben.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**WPD- \_ Ereignis \_ Gerät \_ entfernt**</dt> </dl>                                         | Dieses Ereignis wird gesendet, wenn ein Treiber für ein Gerät entladen wird. In der Regel ist dies das Ergebnis des Geräts, das getrennt wird.<br/> Clients sollten die **iportabledevice** -Schnittstelle und alle [**iportabledeviceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) -Schnittstellen freigeben, die im **WPD- \_ Ereignis \_ Parameter \_ PnP-Geräte- \_ \_ ID** angegeben sind.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**\_ \_ \_ Zurücksetzen des WPD-Ereignisses**</dt> </dl>                                               | Dieses Ereignis zeigt an, dass das Gerät im Begriff ist, zurückgesetzt zu werden, und alle verbundenen Clients sollten ihre Verbindungen mit dem Gerät schließen.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**WPD- \_ Ereignis \_ Objekt \_ hinzugefügt**</dt> </dl>                                               | Dieses Ereignis gibt an, dass ein neues-Objekt auf dem Gerät verfügbar ist.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**WPD- \_ Ereignis \_ Objekt \_ entfernt**</dt> </dl>                                         | Dieses Ereignis wird gesendet, nachdem ein zuvor vorhandenes Objekt vom Gerät entfernt wurde.<br/> Das Objekt kann z. b. ein Inhalts Objekt sein, z. b., dass eine Bilddatei gelöscht wurde. oder es kann sich um ein funktionales Objekt handeln, z. b. Wenn ein neues Speichergerät vom Gerät getrennt wurde.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**WPD- \_ Ereignis \_ Objekt \_ Übertragung \_ angefordert**</dt> </dl>       | Dieses Ereignis wird gesendet, um anzufordern, dass eine Anwendung ein bestimmtes Objekt vom Gerät überträgt.<br/> Bei dem Objekt handelt es sich in der Regel um ein Inhalts Objekt, z. b. eine Bilddatei.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**WPD- \_ Ereignis \_ Objekt \_ aktualisiert**</dt> </dl>                                         | Dieses Ereignis wird gesendet, nachdem ein Objekt aktualisiert wurde, und jeder verbundene Client sollte seine Ansicht des Objekts aktualisieren.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**WPD- \_ Ereignis \_ Dienst Methode ist \_ \_ fertiggestellt.**</dt> </dl>             | Dieses Ereignis wird gesendet, wenn ein Treiber den Aufruf einer Dienst Methode abgeschlossen hat. Dieses Ereignis muss gesendet werden, auch wenn die Methode fehlschlägt. Hierbei handelt es sich um ein internes WPD-DDI-Ereignis, das für keine Anwendungen über [**iportabledevice:: Rat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) oder [**iportabledebug:: Rat**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise)verfügbar ist.<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**WPD- \_ Ereignis \_ Speicher \_ Format**</dt> </dl>                                         | Dieses Ereignis gibt den Fortschritt eines Formatierungs Vorgangs für ein Speicher Objekt an.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
</dt> </dl>

 

 




