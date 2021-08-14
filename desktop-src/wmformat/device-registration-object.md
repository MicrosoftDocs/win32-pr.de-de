---
title: Geräteregistrierungsobjekt
description: Geräteregistrierungsobjekt
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Medienformat-SDK, Geräteregistrierungsobjekte
- Advanced Systems Format (ASF), Geräteregistrierungsobjekte
- ASF (Advanced Systems Format), Geräteregistrierungsobjekte
- Objekte,Geräteregistrierungsobjekte
- Geräteregistrierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4594b17f6824e4e3a9e7690e5ea933e24670e9c8b5d95feb16e555f577f87f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433886"
---
# <a name="device-registration-object"></a>Geräteregistrierungsobjekt

Das Geräteregistrierungsobjekt verwaltet die Geräteregistrierungsdatenbank. Diese Datenbank speichert Informationen zu Netzwerkgeräten, z. B. Set-Top-Videoplayern, die mit dem Clientcomputer verbunden sind. Der Hauptzweck der Geräteregistrierungsdatenbank ist die Verwaltung von Geräten, die das Windows Media DRM 10 for Network Devices-Protokoll verwenden, um gesicherte Datenströme zu empfangen.

Wenn Ihre Anwendung Windows Media DRM 10 für Netzwerkgeräte unterstützt, müssen Sie die Schnittstellen dieses Objekts verwenden, um Netzwerkgeräte zu registrieren und diese Geräte zu überprüfen. Sie können auch die Geräteregistrierungsdatenbank verwenden, um Informationen zu Netzwerkgeräten zu speichern, die Windows Media DRM 10 für Netzwerkgeräte nicht verwenden, obwohl nicht alle Informationen in der Datenbank für solche Geräte gelten.

Das Geräteregistrierungsobjekt wird von der [**WMCreateDeviceRegistration-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) erstellt, die einen Zeiger auf eine **IWMDeviceRegistration-Schnittstelle** legt. Die anderen Methoden des Geräteregistrierungsobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Geräteregistrierungsobjekt unterstützt.



| Schnittstelle                                              | BESCHREIBUNG                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Verwaltet die Geräteregistrierungsdatenbank. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analysiert von Geräten gesendete Nachrichten.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Verwaltet die Geräteüberprüfung.                |



 

Die folgende Rückrufschnittstelle muss von der Anwendung implementiert werden, um die Methoden der **IWMProximityDetection-Schnittstelle verwenden zu** können.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




