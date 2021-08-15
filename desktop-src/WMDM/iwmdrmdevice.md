---
title: IWMDRMDevice-Schnittstelle
description: Diese Schnittstelle ist nicht für die Umsetzung durch einen Dienstanbieter vorgesehen, sondern dient der vollständigen Dokumentation. Die IWMDRMDevice-Schnittstelle ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, die Windows Media DRM 10 für portable Geräte verwenden.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- IWMDRMDevice interface windows Media Geräte-Manager
- IWMDRMDevice interface windows Media Geräte-Manager , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fee40eb6fdada2374b0f571a201ff53fb38f41de7f3cac5eeaa2159475bfdb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005120"
---
# <a name="iwmdrmdevice-interface"></a>IWMDRMDevice-Schnittstelle

Diese Schnittstelle ist nicht für die Umsetzung durch einen Dienstanbieter vorgesehen, sondern dient der vollständigen Dokumentation.

Die **IWMDRMDevice-Schnittstelle** ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, die Windows Media DRM 10 für portable Geräte verwenden.

## <a name="members"></a>Member

Die **IWMDRMDevice-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDevice** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMDevice-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Startet den Prozess der Bereinigung des DRM-Datenspeichers auf dem Gerät.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Ruft das Gerätezertifikat ab.<br/>                                                 |
| [**GetMeterC wiege**](iwmdrmdevice-getmeterchallenge.md)             | Ruft die Messungs-Herausforderung ab.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Ruft die sichere Uhr ab.<br/>                                                       |
| [**GetSecureClockCuhrge**](iwmdrmdevice-getsecureclockchallenge.md) | Ruft die Herausforderung der sicheren Uhr ab.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Ruft die Lizenzsynchronisierungsliste ab.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Bestimmt, ob das Gerät Windows Media DRM 10 für portable Geräte unterstützt.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Legt die Lizenzantwort fest.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Legt die Messungsantwort fest.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Legt die sichere Uhrantwort fest.<br/>                                                   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Dienstanbieter**](interfaces-for-service-providers.md)
</dt> </dl>

 

