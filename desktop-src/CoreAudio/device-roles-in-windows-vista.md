---
description: Arbeiten mit Geräterollen
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: Arbeiten mit Geräterollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7e3d0d2612415ddc3f72571774f11a2d62c911290b156be7efb543c48546e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406893"
---
# <a name="working-with-device-roles"></a>Arbeiten mit Geräterollen

Die [MMDevice-API](mmdevice-api.md) unterstützt Geräterollen. Die [**ERole-Enumeration**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) definiert die Geräterollen, die von der MMDevice-API unterstützt werden.

> [!Note]  
> Obwohl die [MMDevice-API](mmdevice-api.md) Geräterollen unterstützt, implementiert die Benutzeroberfläche in Windows Vista keine Unterstützung für dieses Feature.

 

Eine Anwendung kann die MMDevice-API verwenden, um [Geräterollen](device-roles.md) über die [**METHODEN IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) und [**IMMNotificationClient::OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) zu unterstützen. Die Benutzeroberfläche in Windows Vista unterstützt jedoch nicht die Zuweisung einzelner Rollen zu verschiedenen Geräten. In Windows Vista ermöglicht die Benutzeroberfläche dem Benutzer, ein Standardaudiogerät für das Rendering und ein Standardaudiogerät für die Erfassung auszuwählen. Wenn der Benutzer ein Standardrendering- oder Erfassungsgerät auswählt, weist das System diesem Gerät alle drei Geräterollen (eConsole, eMultimedia und eCommunications) zu. Anwendungen können die Rollen, die Audioendpunktgeräten zugewiesen sind, nicht ändern. Das Betriebssystem erlaubt nur dem Benutzer, Geräterollen zuzuweisen.

Ein Client kann sich registrieren, um bei jeder Änderung bei der Zuweisung von Rollen zu Audioendpunktgeräten eine Benachrichtigung von der MMDevice-API zu erhalten. Wenn eine Rolle von einem Gerät zu einem anderen wechselt, kann der Client auswählen, ob die Streams weiterhin über dasselbe Gerät wiedergegeben (oder aufgezeichnet) werden sollen oder ob die Datenströme auf ein anderes Gerät umgeschaltet werden sollen. Standardmäßig werden die Streams weiterhin über das ursprüngliche Gerät wiedergegeben (oder aufgezeichnet). In Windows Vista muss der Client die Streams auf dem ursprünglichen Gerät löschen und Ersatzdatenströme auf dem neuen Gerät erstellen, um die Streams auf ein anderes Gerät umzustellen. In Windows 7 kann der Client auf neue Benachrichtigungen lauschen, um einen nahtlosen Switch zu implementieren, ohne die Wiedergabe- oder Aufzeichnungssitzung zu unterbrechen. Weitere Informationen finden Sie unter [Streamrouting.](stream-routing.md)

Wenn Sie ihre Anwendung mit Windows Vista testen möchten, können Sie eine Testumgebung einrichten, um zu überprüfen, ob sich die Anwendung wie erwartet verhält, wenn der Benutzer einzelnen Geräterollen verschiedene Geräte zuweisen kann. Sollten Sie weitere Informationen benötigen, senden Sie eine E-Mail an uaa@microsoft.com.

## <a name="communication-devices"></a>Kommunikationsgeräte

Die Windows 7-Benutzeroberfläche verfügt über die Möglichkeit, *Kommunikationsgeräte* hinzuzufügen. Mit  der Sound-Systemsteuerung kann der Benutzer jeweils ein Standardkommunikationsgerät zum Rendern und Erfassen des Audiodatenstroms auswählen. Wenn ein neues Gerät mit dem Computer verbunden ist, führt das Betriebssystem standardmäßig eine automatische Rollenerkennung durch und ermittelt, ob das Gerät für die eCommunication-Rolle geeignet ist. Durch die Ausrichtung auf Kommunikationsgeräte können Sie Anwendungen entwickeln, die Core Audio-APIs verwenden, um PC-Phone-Kommunikationslösungen zu implementieren. Beispielsweise kann eine VoIP-Anwendung ihre Spracheingabe- und Ausgabedatenströme den Standardgeräten für Erfassungs- und Renderingendpunkte mit der Rolle "eCommunications" zuweisen. Wie jeder andere Stream muss eine Kommunikationsanwendung einen Verweis auf den Endpunkt des Kommunikationsgeräts abrufen, indem [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufgerufen wird. In diesem Aufruf muss die Anwendung **eCommunications** im *Role-Parameter* angeben. Die WASAPI-Datenstromvorgänge in einem Stream, der auf einem Kommunikationsgerät geöffnet ist, ähneln jedem anderen Audiostream. Die Kommunikationsanwendung kann die Benutzerfreundlichkeit verbessern, indem Sie Verhaltensweisen implementieren, z. B. Das Verdumern, indem Benachrichtigungen vom Geräteendpunkt verarbeitet werden. Weitere Informationen finden Sie unter [Verwenden eines Kommunikationsgeräts.](using-the-communication-device.md)

## <a name="automatic-device-role-detection"></a>Automatische Erkennung von Geräterollen

Stellen Sie sich ein Szenario vor, in dem ein Computer über ein Standardrenderinggerät, die Lautsprecher und ein Standardaufnahmegerät und ein Mikrofon verfügt. Der Benutzer verbindet ein USB-Headset mit dem Computer. Nachdem die entsprechenden Treiber installiert wurden, versucht das Betriebssystem, eine Rolle zu erkennen, die dem neuen Audiogerät zugewiesen werden soll.

In Windows 7 wurde das Feature zur Erkennung von Geräterollen erheblich verbessert, um die geeigneten Rollen für Audiogeräte zu ermitteln. Alle Audiogeräte enthalten eine Reihe von Konfigurationseinstellungen, die vom Geräte-OEM aufgefüllt werden, die dem System bei der Entscheidung helfen, wie das Gerät verwendet werden soll. Diese Einstellungen umfassen Informationen wie den physischen Speicherort der Audiobuchse, den Gerätetyp, den Untertyp der Buchse und Erkennungsfunktionen, sodass das System bestimmen kann, ob das Gerät angeschlossen ist. Durch das Abrufen dieser Werte vom Gerät bestimmt das Betriebssystem die Rolle, die dem Gerät zugewiesen werden soll. In diesem Szenario hat das System das USB-Headset abgefragt, eine automatische Rollenerkennung durchgeführt und entschieden, dass das Gerät am besten als Kommunikationsgerät geeignet ist.

Eine Anwendung kann auch mithilfe der Core Audio-APIs Jack-Informationen abrufen. Weitere Informationen finden Sie unter [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) und [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräterollen](device-roles.md)
</dt> </dl>

 

 



