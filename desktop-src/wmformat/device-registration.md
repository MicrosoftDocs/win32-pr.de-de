---
title: Geräteregistrierung
description: Geräteregistrierung
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media-Format-SDK, Geräteregistrierung
- Windows Media-Format-SDK, Registrierung von Geräten
- Advanced Systems Format (ASF), Geräteregistrierung
- ASF (Advanced Systems Format), Geräteregistrierung
- Advanced Systems Format (ASF), Registrierung von Geräten
- ASF (Advanced Systems Format), Registrierung von Geräten
- Digital Rights Management (DRM), Geräteregistrierung
- DRM (Digital Rights Management), Geräteregistrierung
- Digital Rights Management (DRM), Registrierung von Geräten
- DRM (Digital Rights Management), Registrierung von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038554"
---
# <a name="device-registration"></a>Geräteregistrierung

Das Windows Media-Format-SDK ermöglicht den Zugriff auf die Geräte Registrierungsdatenbank. Diese Datenbank ist auf dem Client Computer gesichert und wird zum Registrieren von Geräten verwendet, von denen Windows Media DRM 10 für Netzwerkgeräte unterstützt wird.

Wenn ein Gerät zu einem Netzwerk hinzugefügt wird, mit dem der Client Computer verbunden ist, versucht das Gerät, eine Verbindung mit einer Windows Media DRM 10 for Network Devices-Sender Anwendung aufzunehmen. Nach dem Einrichten der Kommunikation sendet das Gerät eine Registrierungs Anforderungs Nachricht.

Die Anwendung sollte die folgenden Schritte ausführen, wenn eine Registrierungs Anforderungs Nachricht empfangen wird:

1.  Analysieren Sie die Nachricht, indem Sie die [**iwmdrmmessageparser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) -Methode aufrufen. Diese Methode ruft das Gerätezertifikat und die Seriennummer des Geräts ab, die beide zum Identifizieren des Geräts benötigt werden.
2.  Nennen Sie die [**iwmdeviceregistration:: getregistereddevicebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) -Methode, und übergeben Sie das Zertifikat und die Geräteserien Nummer, die Sie in Schritt 1 abgerufen haben. Wenn das Gerät gefunden wurde, ist es bereits registriert, und Sie können den nächsten Schritt überspringen.
3.  Wenden Sie die [**iwmdeviceregistration:: registerdevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) -Methode an, um das Gerät der Geräte Registrierungsdatenbank hinzuzufügen.

Sie können auf Informationen zu jedem Gerät in der Registrierungsdatenbank zugreifen, indem Sie das registrierte Geräte Objekt abrufen, das diesem zugeordnet ist. Es gibt zwei Möglichkeiten, ein registriertes Geräte Objekt zu erhalten. Wenn Sie über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie die [**iwmdeviceregistration:: getregistereddevicebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) -Methode aufrufen. Wenn Sie nicht über das Zertifikat und die Seriennummer des Geräts verfügen, können Sie alle Geräte in der Datenbank auflisten, indem Sie [**iwmdeviceregistration:: getfirstregistereddevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) aufrufen, gefolgt von wiederholten Aufrufen von [**iwmdeviceregistration:: getnextregistereddevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) , bis ein Aufruf S false zurückgibt \_ .

Bevor die Anwendung Daten an ein Gerät senden kann, müssen Sie sicherstellen, dass das Gerät genehmigt, überprüft und geöffnet wird.

Die Geräte Genehmigung sollte eine Interaktion mit dem Benutzer beinhalten. Wenn ein Gerät eine Registrierungsmeldung sendet, kann die Anwendung den Benutzer auffordern, zu entscheiden, ob es sich bei dem Gerät um ein Gerät handelt, das die Daten des Benutzers erhalten soll. Aktualisieren Sie dann die Geräte Registrierungsdatenbank, indem Sie die [**iwmregistereddevice:: genehmigen**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) -Methode aufrufen, und übergeben Sie nach Bedarf **true** oder **false** .

Die Validierung wird auch als near-Erkennung bezeichnet. Hierbei handelt es sich um einen Prozess, mit dem die internen DRM-Objekte des Windows Media-SDK ermitteln, ob das Gerät "nah" ist, bis der Computer, auf dem Ihre Anwendung ausgeführt wird, auf sichere Weise Medien überträgt. Die Nähe wird durch die Zeit bestimmt, die benötigt wird, um eine Antwort auf eine Nachricht zu erhalten. Diese Funktion soll verhindern, dass nicht autorisierte Benutzer auf Ihr Netzwerk zugreifen und Ihre gesicherten Medien erhalten. Weitere Informationen finden Sie unter [Durchführen der Near-Erkennung](performing-proximity-detection.md).

Um ein Gerät zu öffnen, nennen Sie [**iwmregistereddevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmregistereddevice**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[**Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




