---
title: Geräteregistrierung
description: Geräteregistrierung
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Medienformat-SDK, Geräteregistrierung
- Windows Medienformat-SDK, Registrierung von Geräten
- Advanced Systems Format (ASF), Geräteregistrierung
- ASF (Advanced Systems Format), Geräteregistrierung
- Advanced Systems Format (ASF), Registrierung von Geräten
- ASF (Advanced Systems Format), Registrierung von Geräten
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Geräteregistrierung
- DRM (Digital Rights Management), Geräteregistrierung
- Verwaltung digitaler Rechte (Digital Rights Management, DRM), Registrierung von Geräten
- DRM (Digital Rights Management), Registrierung von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2efbfefaaabf3af0a33f304ad2cc32f7fe3b84691da8242203eddbb18fdb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027928"
---
# <a name="device-registration"></a>Geräteregistrierung

Das Windows Media Format SDK bietet Zugriff auf die Geräteregistrierungsdatenbank. Diese Datenbank wird auf dem Clientcomputer gesichert und zum Registrieren von Geräten verwendet, die Windows Media DRM 10 für Netzwerkgeräte unterstützen.

Wenn ein Gerät einem Netzwerk hinzugefügt wird, mit dem der Clientcomputer verbunden ist, versucht das Gerät, eine Windows Media DRM 10 for Network Devices-Senderanwendung zu kontaktieren. Nach dem Herstellen der Kommunikation sendet das Gerät eine Registrierungsanforderungsnachricht.

Ihre Anwendung sollte die folgenden Schritte ausführen, wenn sie eine Registrierungsanforderungsnachricht empfängt:

1.  Analysieren Sie die Nachricht, indem Sie [**die IWMDRMMessageParser::P arseRegistrationReqMsg-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) aufrufen. Diese Methode ruft das Gerätezertifikat und die Seriennummer des Geräts ab, die beide zum Identifizieren des Geräts erforderlich sind.
2.  Rufen Sie [**die IWMDeviceRegistration::GetRegisteredDeviceByID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) auf, und übergeben Sie dabei das In Schritt 1 abgerufene Zertifikat und die Seriennummer des Geräts. Wenn das Gerät gefunden wird, ist es bereits registriert, und Sie können den nächsten Schritt überspringen.
3.  Rufen Sie [**die IWMDeviceRegistration::RegisterDevice-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) auf, um das Gerät der Geräteregistrierungsdatenbank hinzuzufügen.

Sie können auf Informationen zu jedem Gerät in der Registrierungsdatenbank zugreifen, indem Sie das zugeordnete registrierte Geräteobjekt abrufen. Es gibt zwei Möglichkeiten, ein registriertes Geräteobjekt zu erhalten. Wenn Sie über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie die [**IWMDeviceRegistration::GetRegisteredDeviceByID-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) aufrufen. Wenn Sie nicht über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie alle Geräte in der Datenbank aufzählen, indem Sie [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) gefolgt von wiederholten Aufrufen von [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) aufrufen, bis ein Aufruf S \_ FALSE zurückgibt.

Bevor Ihre Anwendung Daten an ein Gerät senden kann, müssen Sie sicherstellen, dass das Gerät genehmigt, überprüft und geöffnet ist.

Die Gerätegenehmigung sollte eine Interaktion mit dem Benutzer umfassen. Wenn ein Gerät eine Registrierungsnachricht sendet, kann Ihre Anwendung den Benutzer auffordern, zu entscheiden, ob es sich um ein Gerät handelt, das die Daten dieses Benutzers empfangen soll. Aktualisieren Sie dann die Geräteregistrierungsdatenbank, indem Sie [**die IWMRegisteredDevice::Approve-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) aufrufen und **dabei TRUE** oder **FALSE** übergeben.

Die Validierung wird auch als Näherungserkennung bezeichnet. Dies ist ein Prozess, bei dem die internen DRM-Objekte des Windows Media Format SDK bestimmen, ob das Gerät dem Computer, auf dem Ihre Anwendung ausgeführt wird, "nah" genug ist, um Medien sicher zu übertragen. Die Nähe wird durch die Zeit bestimmt, die benötigt wird, um eine Antwort auf eine Nachricht zu erhalten. Dieses Feature soll verhindern, dass nicht autorisierte Benutzer auf Ihr Netzwerk zugreifen und Ihre geschützten Medien abrufen. Weitere Informationen finden Sie unter [Ausführen der Näherungserkennung.](performing-proximity-detection.md)

Um ein Gerät zu öffnen, rufen Sie [**IWMRegisteredDevice::Open auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMRegisteredDevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Verwenden des Windows Media DRM 10 for Network Devices Protocol**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




