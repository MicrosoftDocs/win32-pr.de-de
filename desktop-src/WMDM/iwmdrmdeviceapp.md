---
title: IWMDRMDeviceApp-Schnittstelle
description: Die IWMDRMDeviceApp-Schnittstelle ermöglicht es einer Anwendung, DRM-Komponenten eines Geräts zu vermessung, Lizenzen zu synchronisieren und zu aktualisieren.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- IWMDRMDeviceApp-Schnittstelle windows Media Geräte-Manager
- IWMDRMDeviceApp-Schnittstelle Windows Media Geräte-Manager , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d618a0534592ebe01a961ba9b0fdd462fcda70597b5f909b30e8fb92f6bdbeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055628"
---
# <a name="iwmdrmdeviceapp-interface"></a>IWMDRMDeviceApp-Schnittstelle

\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden. Verwenden [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) stattdessen .\]

Die **IWMDRMDeviceApp-Schnittstelle** ermöglicht es einer Anwendung, DRM-Komponenten eines Geräts zu vermessung, Lizenzen zu synchronisieren und zu aktualisieren. Diese Schnittstelle funktioniert nur mit Geräten, die Windows Media DRM 10 für portable Geräte unterstützen.

Um diese Schnittstelle zu erhalten, rufen **Sie CoCreateInstance auf,** und übergeben Sie CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Diese Schnittstelle wird in der Headerdatei definiert, die aus WMDRMDeviceApp.idl erstellt wurde. Dieser Header **\# enthält** s "wmdm.h". Möglicherweise müssen Sie diesen Dateinamen so ändern, dass er mit dem Header aus WMDM.idl übereinstimmen kann.

 

## <a name="members"></a>Member

Die **IWMDRMDeviceApp-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDeviceApp** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMDeviceApp-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                   | Beschreibung                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Initialisiert oder setzt eine sichere Geräteuhr zurück.<br/>                                                                                     |
| [**GenerateMeterC wiege**](iwmdrmdeviceapp-generatemeterchallenge.md) | Übernimmt Messungsdaten von einem Gerät.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Setzt einige oder alle Messzahlen auf einem Gerät zurück, nachdem Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Fragt ein Gerät nach seinem aktuellen DRM-Status und seinen Funktionen ab.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Aktualisiert Lizenzen auf einem Gerät, wenn diese kurz vor dem Ende stehen.<br/>                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> <dt>

[**Nutzung von Messungsinhalten**](metering-content-usage.md)
</dt> </dl>

 

