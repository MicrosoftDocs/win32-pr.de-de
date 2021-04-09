---
description: Zugriffssteuerung
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868272"
---
# <a name="access-control-wpd-api"></a>Access Control (WPD-API)

Der Windows-Treibermodell (WDM) unterstützt die Beschränkung des Geräte Zugriffs über Access Control Listen (ACLs) auf dem Plug & Play (PNP)-Geräteknoten. Dies bedeutet, dass Anbieter und Netzwerkadministratoren den Zugriff auf jeden Gerätetyp einschränken können. Wenn eine Anwendung ein Handle für einen Treiber durch Aufrufen von [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)öffnet, überprüft der e/a-Manager des Treibers, ob der angegebene Benutzer über die erforderlichen Zugriffsrechte verfügt, und auf ähnliche Weise prüft der Zugriff, wenn IOCTLs von diesem Handle an den Treiber gesendet wird.

Ein Netzwerkadministrator könnte beispielsweise Gastbenutzer auf den schreibgeschützten Zugriff für tragbare Geräte beschränken und authentifizierten Benutzern Lese-/Schreibzugriff gewähren. In diesem Fall bedeutet dies, dass ein Gast einen WPD-Befehl ausgegeben hat, der Lese-/Schreibzugriff erforderte (z. b. Delete-Objekt). der Fehler tritt auf, wenn ein authentifizierter Benutzer denselben Befehl ausgegeben hat.

Die Gruppenrichtlinie Einträge zum Steuern des Zugriffs auf Wechselmedien und tragbare Geräte sind tatsächlich nichts anderes als eine einfache Möglichkeit für Administratoren, PNP-Geräteknoten-ACLs gleichzeitig auf eine ganze Klasse von Geräten anzuwenden (z. b. durch Anwenden der "Schreibzugriff auf tragbare Geräte verweigern" Gruppenrichtlinie die ACLs aller WPD-Geräte so anpassen, dass der Schreibzugriff verweigert wird).

## <a name="io-control-codes-in-wpd"></a>E/a-Steuerungs Codes in WPD

WPD-Anwendungen kommunizieren mit Treibern, indem Sie Geräte Handles öffnen und e/a-Kontroll Codes (IOCTLs) senden. Diese IOCTLs bestehen aus vier Abschnitten:

1.  Gerätetyp
2.  Funktions Code
3.  Buffer-Methode
4.  Zugriffstyp

Der vierte Abschnitt, der Zugriffstyp, gibt die jeweilige Zugriffs Anforderung für den angegebenen Befehl an. Der e/a-Manager des Treibers verwendet diese Daten zum Durchführen der Überprüfung der Access Control Liste (ACL).

Wenn ein IOCTL-Element wie folgt definiert wurde:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



Der e/a-Manager des Treibers prüft, ob der Besitzer des Geräte Handles über Lesezugriff auf das Gerät verfügt, wenn diese Nachricht gesendet wird.

Und, wenn eine ioctl definiert wurde:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



Der e/a-Manager des Treibers prüft, ob der Besitzer des Geräte Handles Lese-/Schreibzugriff auf das Gerät hat, wenn diese Nachricht gesendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> <dt>

[**Iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**Iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



