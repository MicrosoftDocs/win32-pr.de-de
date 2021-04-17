---
title: Iwmdrmdevice-Schnittstelle
description: Diese Schnittstelle ist nicht dafür vorgesehen, von einem Dienstanbieter implementiert zu werden. Sie wird jedoch für eine komplette Dokumentation bereitgestellt. Die iwmdrmdevice-Schnittstelle ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte verwendet wird.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315476"
---
# <a name="iwmdrmdevice-interface"></a>Iwmdrmdevice-Schnittstelle

Diese Schnittstelle ist nicht dafür vorgesehen, von einem Dienstanbieter implementiert zu werden. Sie wird jedoch für eine komplette Dokumentation bereitgestellt.

Die **iwmdrmdevice** -Schnittstelle ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte verwendet wird.

## <a name="members"></a>Member

Die **iwmdrmdevice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmdevice** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmdevice** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Cleandatastore**](iwmdrmdevice-cleandatastore.md)                   | Startet die Bereinigung des DRM-Datenspeicher auf dem Gerät.<br/>                  |
| [**Getde vicecertificate**](iwmdrmdevice-getdevicecertificate.md)       | Ruft das Gerätezertifikat ab.<br/>                                                 |
| [**Getmeterchallenge**](iwmdrmdevice-getmeterchallenge.md)             | Ruft die Messungs Herausforderung ab.<br/>                                                 |
| [**Getsecureclock**](iwmdrmdevice-getsecureclock.md)                   | Ruft die sichere Uhr ab.<br/>                                                       |
| [**Getsecureclockchallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Ruft die Anforderung der sicheren Uhr ab.<br/>                                             |
| [**Getsynclist**](iwmdrmdevice-getsynclist.md)                         | Ruft die Lizenz Synchronisierungs Liste ab.<br/>                                       |
| [**Iswmdrmdevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Legt die Lizenz Antwort fest.<br/>                                                        |
| [**Setmeterresponse**](iwmdrmdevice-setmeterresponse.md)               | Legt die Messungs Antwort fest.<br/>                                                       |
| [**Setsecureclockresponse**](iwmdrmdevice-setsecureclockresponse.md)   | Legt die Antwort auf die sichere Uhr fest.<br/>                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Dienstanbieter**](interfaces-for-service-providers.md)
</dt> </dl>

 

