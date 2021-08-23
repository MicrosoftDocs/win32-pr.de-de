---
description: Zugriffssteuerung
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83caa01b08409afd196ea0507cb47986928a1d947b6ff7907640e4f9bd5b390f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657910"
---
# <a name="access-control-wpd-api"></a>Access Control (WPD-API)

Das Windows Driver Model (WDM) unterstützt das Einschränken des Gerätezugriffs über Access Control Lists (ACLs) auf den Plug & Play-Geräteknoten (PnP). Dies bedeutet, dass Anbieter und Netzwerkadministratoren den Zugriff auf jeden Gerätetyp einschränken können. Wenn eine Anwendung ein Handle für einen Treiber öffnet, indem [**sie IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)aufruft, überprüft der E/A-Manager des Treibers, ob der entsprechende Benutzer über den erforderlichen Zugriff verfügt, und führt ebenso Zugriffsüberprüfungen durch, wenn IOCTLs von diesem Handle an den Treiber gesendet werden.

Beispielsweise könnte ein Netzwerkadministrator Gastbenutzern den schreibgeschützten Zugriff auf portable Geräte gewähren, während sie authentifizierten Benutzern Lese-/Schreibzugriff gewähren könnten. In diesem Fall impliziert dies, dass , wenn ein Gast einen WPD-Befehl ausgegeben hat, der Lese-/Schreibzugriff erforderte (z. B. Objekt löschen). Dies würde mit "Zugriff verweigert" fehlschlagen. Wenn ein authentifizierter Benutzer denselben Befehl aussinge, wäre dies jedoch erfolgreich.

Die Gruppenrichtlinie-Einträge zum Steuern des Zugriffs auf Wechseldatenträger und portable Geräte sind eigentlich nur eine einfache Möglichkeit für Administratoren, PnP-Geräteknoten-ACLs gleichzeitig auf eine ganze Geräteklasse anzuwenden (z. B. würde die Anwendung von "Schreibzugriff auf portable Geräte verweigern" Gruppenrichtlinie die ACLs aller WPD-Geräte anpassen, um den Schreibzugriff zu verweigern).

## <a name="io-control-codes-in-wpd"></a>E/A-Steuerungscodes in WPD

WPD-Anwendungen kommunizieren mit Treibern, indem sie Gerätehandles öffnen und E/A-Steuerungscodes (IOCTLs) senden. Diese IOCTLs bestehen aus vier Abschnitten:

1.  Gerätetyp
2.  Funktionscode
3.  Buffer-Methode
4.  Zugriffstyp

Der vierte Abschnitt, der Zugriffstyp, gibt die spezifische Zugriffsanforderung für den angegebenen Befehl an. Der E/A-Manager des Treibers verwendet diese Daten, um die Überprüfung Access Control -Liste (ACL) durchzuführen.

Wenn also eine IOCTL wie dies definiert wurde:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



Der E/A-Manager des Treibers überprüft, ob der Besitzer des Gerätehandles beim Senden dieser Nachricht Über lesezugriff auf das Gerät hat.

Und wenn eine IOCTL wie dies definiert wurde:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



Der E/A-Manager des Treibers überprüft beim Senden dieser Nachricht, ob der Besitzer des Gerätehandles über Lese-/Schreibzugriff auf das Gerät verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> <dt>

[**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



