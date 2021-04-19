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
# <a name="device-interface-guids"></a>Geräteschnittstellen-GUIDs

Die Geräteschnittstelle kann durch einen **GUID** -Wert beschrieben werden. Tragbare Windows-Geräte definieren die folgende Geräteschnittstelle.



| Konstante                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID- \_ devinterface- \_ WPD**</dt> </dl>                          | Identifiziert Geräte, die in einer normalen WPD-Enumeration angezeigt werden. Alle Geräte, die diese Schnittstellen-GUID registrieren, werden aufgezählt, wenn eine Anwendung die [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) -Methode aufruft.<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ devinterface- \_ WPD \_ Privat**</dt> </dl> | Identifiziert Geräte, die während einer normalen WPD-Enumeration nicht angezeigt werden. Alle Geräte, die diese Schnittstellen-GUID registrieren, werden nur aufgelistet, wenn eine Anwendung die [**iportabledevicemanager:: getprivatedevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) -Methode aufruft.<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID- \_ devinterface- \_ WPD- \_ Dienst**</dt> </dl> | In Windows 7 können Anwendungen alle WPD-Geräte Dienste auflisten, indem Sie [**iportabledeviceservicemanager:: getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) aufrufen und diese Schnittstellen Klasse als Diensttyp-GUID verwenden.<br/>                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




