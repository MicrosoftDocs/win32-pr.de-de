---
title: Geräte Anbieter
description: Geräte Anbieter sind registrierte Objekte, die bei jedem Systemstart gestartet werden.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101751"
---
# <a name="device-providers"></a>Geräte Anbieter

Geräte Anbieter sind registrierte Objekte, die bei jedem Systemstart gestartet werden. Geräte Anbieter registrieren und heben die Registrierung ausgelaufener Geräte beim Geräte Host als Reaktion auf ein Ereignis auf. Diese Geräte sind Geräte, die beim Systemstart automatisch gestartet wurden. Aus Sicherheitsgründen sollte ein Geräte Anbieter normalerweise als " [LocalService](/windows/desktop/Services/localservice-account)" und nicht als " [LocalSystem](/windows/desktop/Services/localsystem-account)" ausgeführt werden.

Geräte Anbieter können für vorübergehende Geräte verwendet werden. Geräte Anbieter können auch verwendet werden, um Geräte mit abzurufenden Medien zu überbrücken. Beispielsweise ist ein Peripheriegerät, z. b. ein Digital Music Player, über einen seriellen Anschluss mit einem Computer verbunden. Um den Music Player als UPnP-basiertes Gerät verfügbar zu machen, sind ein Geräte Steuerungsobjekt und ein Satz von Dienst Objekten erforderlich. Diese Objekte implementieren die UPnP-basierten Musikplayer Aktionen als serielle Befehle. Der Musikplayer muss jedoch an den seriellen Anschluss angeschlossen und zur Steuerung verfügbar sein, bevor diese Objekte registriert werden.

Da der serielle Port keinen expliziten Benachrichtigungs Mechanismus bietet, wenn Geräte verbunden sind, ist Abruf Code erforderlich. Dieser Code kann in einem Geräte Anbieter Objekt, einem Dienst oder in einer eigenständigen Anwendung implementiert werden. Wenn der Computer gestartet wird, instanziiert der Geräte Host das Geräte Anbieter Objekt und ruft dann seine [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) -Methode auf. Wenn der Geräte Anbieter das vorhanden sein eines Music Player-Geräts erkennt, instanziiert er das entsprechende Geräte Steuerungsobjekt und registriert es durch Aufrufen von [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Diese Methode veröffentlicht das Gerät und kündigt es dem UPnP-basierten Netzwerk an.

Die gleiche Funktionalität kann auch durch Implementieren eines Dienstanbieter erreicht werden, der den seriellen Anschluss abruft. Geräte Anbieter vereinfachen jedoch Dinge, indem Sie nur die Kernfunktionen – die Abruf –, die implementiert werden müssen, weil Geräte Anbieter den Geräte Host zum Starten und zum Starten benötigen. Die Verwendung von Geräte Anbietern ist einfacher als die Implementierung eines Dienstes.

Beim Registrierungs Zeitpunkt und bei jedem nachfolgenden Systemstart instanziiert der Computer das Geräte Anbieter Objekt und ruft dann die [**iupnpdeviceprovider:: Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) -Methode auf und übergibt dabei die während der Registrierung angegebene Initialisierungs Zeichenfolge.

Nachdem die [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) -Methode aufgerufen wurde, führt der Geräte Anbieter alle erforderlichen Verarbeitungsschritte aus. wenn dies erforderlich ist, registriert der Geräte Anbieter Geräte durch Aufrufen von [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), wie im Abschnitt [Registrieren eines gehosteten Geräts beim Geräte Host](registering-a-hosted-device-with-the-device-host.md)beschrieben.

Wenn der Computer heruntergefahren wird, ruft der Geräte Host die [**iupnpdeviceprovider::**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) End-Methode auf, um anzugeben, dass der Geräte Anbieter seine Vorgänge beendet.

 

 