---
description: Endpunkt-ID-Zeichenfolgen
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Endpunkt-ID-Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fdfbf12f3e037a23163bb3e8fef525db89c15904328c9e0fd8a71e5de004b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957309"
---
# <a name="endpoint-id-strings"></a>Endpunkt-ID-Zeichenfolgen

In Windows Vista generiert das System Endpunkt-ID-Zeichenfolgen, um die [Audioendpunktgeräte](audio-endpoint-devices.md) im System zu identifizieren. Eine Endpunkt-ID-Zeichenfolge ist eine auf NULL endende Breitzeichenzeichenfolge. Die Endpunkt-ID-Zeichenfolge für ein bestimmtes Audioendpunktgerät identifiziert das Gerät eindeutig unter allen Audioendpunktgeräten im System.

Wenn ein System zwei oder mehr identische Audioadaptergeräte enthält, haben die entsprechenden Audioendpunktgeräte identische Anzeigenamen, aber jedes Endpunktgerät verfügt über eine eindeutige Endpunkt-ID-Zeichenfolge. Weitere Informationen zum Abrufen des Anzeigenamens eines Endpunktgeräts finden Sie unter [Geräteeigenschaften.](device-properties.md)

Nach dem Abrufen einer [**IMMDevice-Schnittstelleninstanz**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) für ein Audioendpunktgerät kann ein Client die [**IMMDevice::GetId-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) aufrufen, um die Endpunkt-ID-Zeichenfolge für das Gerät abzurufen. Ein Client kann die Endpunkt-ID-Zeichenfolge verwenden, um eine Instanz des Audioendpunktgeräts zu einem späteren Zeitpunkt oder in einem anderen Prozess zu erstellen, indem er die [**IMMDeviceEnumerator::GetDevice-Methode aufruft.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)

Ein Client kann eine Benachrichtigung erhalten, wenn sich der Status eines Audioendpunktgeräts ändert. Um Benachrichtigungen zu empfangen, implementiert der Client eine [**IMMNotificationClient-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) und registriert diese Schnittstelle bei der MMDevice-API. Wenn sich der Status eines Endpunktgeräts ändert, ruft die MMDevice-API die entsprechende Methode in der [**EDataFlow-Schnittstelle**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) des Clients auf. Einer der Eingabeparameter für die -Methode ist die Endpunkt-ID-Zeichenfolge, die das Endpunktgerät identifiziert, dessen Status sich geändert hat. Weitere Informationen zu **EDataFlow** finden Sie unter [Geräteereignisse.](device-events.md)

Ältere Audio-APIs wie DirectSound und die Windows Multimediafunktionen verfügen über eigene Schnittstellen zum Aufzählen und Identifizieren von Audiogeräten. In Windows Vista wurden diese Schnittstellen erweitert, um die Endpunkt-ID-Zeichenfolgen anzugeben, die die Endpunktgeräte identifizieren, die den von den APIs dargestellten Geräteabstraktionen zugrunde stehen.

Während der DirectSound-Geräteenumeration stellt DirectSound die Endpunkt-ID-Zeichenfolge für jedes Gerät zur Verfügung, das es aufzählt. Weitere Informationen finden Sie unter [Audioereignisse für Ältere Audioanwendungen.](audio-events-for-legacy-audio-applications.md)

Verwenden Sie zum Abrufen der Endpunkt-ID-Zeichenfolge für ein älteres Wellenformgerät die [**WaveOutMessage-**](/previous-versions//dd743865(v=vs.85)) oder [**waveInMessage-Funktion,**](/previous-versions//dd743846(v=vs.85)) um eine DRV \_ QUERYFUNCTIONINSTANCEID-Nachricht an den Waveform-Gerätetreiber zu senden. Ein Codebeispiel, das die Verwendung dieser Meldung zeigt, finden Sie unter [Geräterollen für Legacy-Windows Multimediaanwendungen.](device-roles-for-legacy-windows-multimedia-applications.md)

Weitere Informationen zur Verwendung der Funktionen der Kernaudio-APIs zum Verbessern von Anwendungen, die Legacyaudio-APIs verwenden, finden Sie unter [Interoperabilität mit Legacyaudio-APIs.](interoperability-with-legacy-audio-apis.md)

Clients sollten den Inhalt der Endpunkt-ID-Zeichenfolge als nicht transparent behandeln. Das heißt, Clients sollten nicht versuchen, den Inhalt der Zeichenfolge zu analysieren, um Informationen zum Gerät abzurufen. Der Grund dafür ist, dass das Zeichenfolgenformat nicht definiert ist und sich von einer Implementierung des MMDevice-API-Systemmoduls zur nächsten ändern kann.

Die Lebensdauer einer Endpunkt-ID-Zeichenfolge ist an die Geräteinstallation gebunden. Die Endpunkt-ID-Zeichenfolge eines Geräts ändert sich, wenn der Benutzer den Gerätetreiber aktualisiert oder wenn der Benutzer das Gerät deinstalliert und erneut installiert. Die Endpunkt-ID-Zeichenfolge bleibt jedoch bei systemübergreifenden Neustarts unverändert, und die Endpunkt-ID-Zeichenfolge eines USB-Audiogeräts bleibt unverändert, wenn der Benutzer das Gerät entpackt und wieder einsteckt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 
