---
title: Iwmdrmdeviceapp-Schnittstelle
description: Die iwmdrmdeviceapp-Schnittstelle ermöglicht es einer Anwendung, Lizenzen zu messen, zu synchronisieren und die DRM-Komponenten eines Geräts zu aktualisieren.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339511"
---
# <a name="iwmdrmdeviceapp-interface"></a>Iwmdrmdeviceapp-Schnittstelle

\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden. Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Die **iwmdrmdeviceapp** -Schnittstelle ermöglicht es einer Anwendung, Lizenzen zu messen, zu synchronisieren und die DRM-Komponenten eines Geräts zu aktualisieren. Diese Schnittstelle funktioniert nur mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte unterstützt wird.

Um diese Schnittstelle zu erhalten, wenden Sie **cokreateinstance** an, und übergeben Sie CLSID \_ wmdrmdeviceapp.

> [!Note]  
> Diese Schnittstelle ist in der Header Datei definiert, die aus wmdrmdeviceapp. idl erstellt wurde. Dieser Header **\# enthält**"WMDM. h". Möglicherweise müssen Sie diesen Dateinamen ändern, damit er mit dem aus WMDM. idl erstellten Header identisch ist.

 

## <a name="members"></a>Member

Die **iwmdrmdeviceapp** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmdeviceapp** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmdeviceapp** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md)           | Initialisiert oder setzt eine sichere Uhr des Geräts zurück.<br/>                                                                                     |
| [**Generatemeterchallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Hiermit werden Messungs Daten von einem Gerät angefordert.<br/>                                                                                           |
| [**Processmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.<br/> |
| [**Querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.<br/>                                                                   |
| [**Synchronizelicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Aktualisiert Lizenzen auf einem Gerät, wenn Sie bald ablaufen.<br/>                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Schnittstellen für Anwendungen**](interfaces-for-applications.md)
</dt> <dt>

[**Verwendung von Messungs Inhalten**](metering-content-usage.md)
</dt> </dl>

 

