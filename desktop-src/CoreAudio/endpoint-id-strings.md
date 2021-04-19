---
description: Endpunkt-ID
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Endpunkt-ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04c07da78b92795ebadd7d8f9731f7188ae8dc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342573"
---
# <a name="endpoint-id-strings"></a>Endpunkt-ID

In Windows Vista generiert das System Endpunkt-ID-Zeichen folgen, um die [audioendpunktgeräte](audio-endpoint-devices.md) im System zu identifizieren. Eine Endpunkt-ID-Zeichenfolge ist eine NULL-terminierte Zeichenfolge mit breit Zeichen. Die Endpunkt-ID-Zeichenfolge für ein bestimmtes audioendpunktgerät identifiziert das Gerät eindeutig zwischen allen audioendpunktgeräten im System.

Wenn ein System mindestens zwei identische audioadaptergeräte enthält, haben die entsprechenden audioendpunktgeräte identische anzeigen Amen, aber jedes Endpunktgerät weist eine eindeutige Zeichenfolge mit Endpunkt-IDs auf. Weitere Informationen zum Abrufen des anzeigen Amens eines Endpunkt Geräts finden Sie unter [Geräteeigenschaften](device-properties.md).

Nachdem eine [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstellen Instanz für ein audioendpunktgerät abgerufen wurde, kann ein Client die [**immdevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) -Methode aufrufen, um die Endpunkt-ID-Zeichenfolge für das Gerät zu erhalten. Ein Client kann die Zeichenfolge der Endpunkt-ID verwenden, um eine Instanz des audioendpunktgeräts zu einem späteren Zeitpunkt oder in einem anderen Prozess zu erstellen, indem die [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode aufgerufen wird.

Ein Client kann anordnen, eine Benachrichtigung zu erhalten, wenn sich der Status eines beliebigen audioendpunktgeräts ändert. Zum Empfangen von Benachrichtigungen implementiert der Client eine [**immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) -Schnittstelle und registriert diese Schnittstelle bei der mmdevice-API. Wenn sich der Status eines Endpunkt Geräts ändert, ruft die mmdevice-API die entsprechende Methode in der [**edataflow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) -Schnittstelle des Clients auf. Einer der Eingabeparameter für die-Methode ist die Endpunkt-ID-Zeichenfolge, die das Endpunkt Gerät identifiziert, dessen Status sich geändert hat. Weitere Informationen zu **edataflow** finden Sie unter [Geräte Ereignisse](device-events.md).

Ältere Audio-APIs wie DirectSound und die Multimedia-Funktionen von Windows verfügen über eigene Schnittstellen zum Auflisten und Identifizieren von Audiogeräten. In Windows Vista wurden diese Schnittstellen so erweitert, dass Sie die Endpunkt-ID-Zeichen folgen bereitstellen, die die Endpunkt Geräte identifizieren, die den von den APIs dargestellten Geräte Abstraktionen zugrunde liegen.

Während der DirectSound-Geräte Enumeration liefert DirectSound die Endpunkt-ID-Zeichenfolge für jedes aufgezählte Gerät. Weitere Informationen finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).

Um die Endpunkt-ID-Zeichenfolge für ein Legacy-Wellenform-Gerät abzurufen, verwenden Sie die [**waveoutmessage**](/previous-versions//dd743865(v=vs.85)) -oder [**waveinmessage**](/previous-versions//dd743846(v=vs.85)) -Funktion, um eine drv \_ -queryfunctioninstanceid-Meldung an den Wellenform-Gerätetreiber zu senden Ein Codebeispiel, in dem die Verwendung dieser Nachricht veranschaulicht wird, finden Sie unter [Geräte Rollen für ältere Windows-Multimediaanwendungen](device-roles-for-legacy-windows-multimedia-applications.md).

Weitere Informationen zur Verwendung der Funktionen der Kerncode-APIs zum Verbessern von Anwendungen, die Legacy-audioapis verwenden, finden Sie unter [Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md).

Clients sollten den Inhalt der Endpunkt-ID-Zeichenfolge als nicht transparent behandeln. Das heißt, Clients sollten nicht versuchen, den Inhalt der Zeichenfolge zu analysieren, um Informationen über das Gerät zu erhalten. Der Grund hierfür ist, dass das Zeichen folgen Format nicht definiert ist und sich von einer Implementierung des mmdevice-API-System Moduls zur nächsten ändern kann.

Die Lebensdauer einer Endpunkt-ID-Zeichenfolge ist an die Geräteinstallation gebunden. Die Endpunkt-ID-Zeichenfolge eines Geräts ändert sich, wenn der Benutzer den Gerätetreiber aktualisiert oder wenn der Benutzer das Gerät deinstalliert und erneut installiert. Allerdings bleibt die Endpunkt-ID-Zeichenfolge bei Systemneustarts unverändert, und die Endpunkt-ID-Zeichenfolge eines USB-Audiogeräts bleibt unverändert, wenn der Benutzer die Plug-ins des Geräts abschließt und wieder einfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 
