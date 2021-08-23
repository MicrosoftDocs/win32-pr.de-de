---
description: Die Geräteschnittstelle kann durch einen GUID-Wert beschrieben werden. Windows Portable Geräte definieren die folgende Geräteschnittstelle.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: Geräteschnittstellen-GUIDs (PortableDevice.h)
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
ms.openlocfilehash: 6f4bd170aeae46f738f5ce4a5a98bc694583a19fe3e7fa6eccc21c86fdc871d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657920"
---
# <a name="device-interface-guids"></a>Geräteschnittstellen-GUIDs

Die Geräteschnittstelle kann durch einen **GUID-Wert** beschrieben werden. Windows Portable Geräte definieren die folgende Geräteschnittstelle.



| Konstante                                                                                                                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD**</dt> </dl>                          | Identifiziert Geräte, die in einer normalen WPD-Enumeration angezeigt werden. Jedes Gerät, das diese Schnittstellen-GUID registriert, wird aufzählt, wenn eine Anwendung die [**IPortableDeviceManager::GetDevices-Methode aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)<br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ PRIVATE**</dt> </dl> | Identifiziert Geräte, die während einer normalen WPD-Enumeration nicht angezeigt werden. Jedes Gerät, das diese Schnittstellen-GUID registriert, wird nur aufzählt, wenn eine Anwendung die [**IPortableDeviceManager::GetPrivateDevices-Methode aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices)<br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <dt>**GUID \_ DEVINTERFACE \_ WPD \_ SERVICE**</dt> </dl> | In Windows 7 können Anwendungen alle WPD-Gerätedienste aufzählen, indem [**sie IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) aufrufen und diese Schnittstellenklasse als Diensttyp-GUID verwenden.<br/>                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




