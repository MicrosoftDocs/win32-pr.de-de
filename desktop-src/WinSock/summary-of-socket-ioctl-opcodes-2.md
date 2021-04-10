---
description: Einige der socketioctl-Opcodes für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Zusammenfassung der socketioctl-OpCodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2243457ddbb7e0bb59f14357cf61d2e771c6a7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131164"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Zusammenfassung der socketioctl-OpCodes

Einige der socketioctl-Opcodes für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst. Ausführlichere Informationen finden Sie in der Winsock-Referenz zu [**Winsock IOCTLs**](winsock-ioctls.md) und der [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) -Funktion. Es gibt weitere neue Protokoll spezifische ioctl-Opcodes, die im Protokoll spezifischen Anhang zu finden sind.

Eine komplette Liste der [**Winsock IOCTLs**](winsock-ioctls.md) finden Sie in der Winsock-Referenz.



| Opcode                                                      | Eingabetyp                               | Ausgabetyp                                 | Bedeutung                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Unsigned long                            | <Not used>                            | Aktiviert oder deaktiviert den nicht blockierenden Modus für den Socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Unsigned long                               | Bestimmt die Datenmenge, die atomarisch vom Socket gelesen werden kann.                                                                                                                                         |
| Siocatmark                                                  | <Not used>                         | BOOL                                        | Bestimmt, ob alle OOB-Daten gelesen wurden.                                                                                                                                                              |
| Zuordnen des Zuordnungs \_ \_ Handles                                      | Begleitende API-abhängig                  | <Not used>                            | Ordnet den Socket dem angegebenen Handle einer Begleit Schnittstelle zu.                                                                                                                                          |
| SIO \_ Aktivieren von \_ zirkulären \_ Warteschlangen                             | <Not used>                         | <Not used>                            | Ermöglicht zirkuläre Warteschlangen.                                                                                                                                                                                          |
| SIO \_ - \_ Route suchen                                            | [**sockaddr**](sockaddr-2.md) -Struktur | <Not used>                            | Fordert an, dass die Route an die angegebene Adresse ermittelt werden soll.                                                                                                                                                      |
| SIO-Leerung \_                                                  | <Not used>                         | <Not used>                            | Verwirft den aktuellen Inhalt der Sende Warteschlange.                                                                                                                                                                    |
| über \_ \_ tragen der Broadcast-Broadcast \_ Adresse                                | <Not used>                         | [**sockaddr**](sockaddr-2.md) -Struktur    | Ruft die Protokoll spezifische Broadcast Adresse ab, die in [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))verwendet werden soll.                                                                                                                  |
| QoS für "sio" \_ \_                                               | <Not used>                         | [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Ruft die aktuellen Fluss Spezifikationen für den Socket ab.                                                                                                                                                              |
| \_ \_ \_ QoS für die QoS-Gruppe                                        | <Not used>                         | [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Reserviert.                                                                                                                                                                                                          |
| SIO \_ Multipoint \_ Loopback                                   | BOOL                                     | <Not used>                            | Steuert, ob Daten, die in einer Multipoint-Sitzung gesendet werden, auch vom gleichen Socket auf dem lokalen Host empfangen werden.                                                                                                     |
| SIO- \_ Multicast \_ Bereich                                       | INT                                      | <Not used>                            | Gibt den Bereich an, in dem Multicast Übertragungen stattfinden.                                                                                                                                                 |
| QoS für die SIO- \_ Gruppe \_                                               | [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Legt neue Fluss Spezifikationen für den Socket fest.                                                                                                                                                                |
| \_ \_ QoS der Gruppe "sio" \_                                        | [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Reserviert.                                                                                                                                                                                                          |
| SIO \_ - \_ handle übersetzen                                      | INT                                      | Begleit-API-abhängig                     | Ruft ein entsprechendes Handle für Socket *s* ab, das im Kontext einer Begleit Schnittstelle gültig ist.                                                                                                               |
| SIO- \_ Routing \_ Schnittstellen \_ Abfrage                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Ruft die Adresse der lokalen Schnittstelle ab, die zum Senden an die angegebene Adresse verwendet werden soll.                                                                                                                   |
| \_Änderung der Routing \_ Schnittstelle \_ von SIO                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Fordert eine Benachrichtigung über Änderungen der Informationen an, \_ die über die-Routing \_ Schnittstellen \_ Abfrage für die angegebene Adresse gemeldet wurden.                                                                                         |
| [**Abfrage für die SIO- \_ Adress \_ Liste \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**\_Socketadresse**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Ruft eine Liste der lokalen Transport Adressen der Protokollfamilie des Sockets ab, an die die Anwendung gebunden werden kann. Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen. |
| Änderung der Liste der in der \_ \_ Liste \_                                  | <Not used>                         | <Not used>                            | Fordert eine Benachrichtigung über Änderungen der Informationen an, die über die Bericht \_ \_ erlisten Abfrage "- \_                                                                                                                         |
| \_Abfrage- \_ pnp- \_ Ziel \_ Handle für SIO                             | <Not used>                         | Glühbirne                                      | Ruft den socketdeskriptor des nächsten Anbieters in der Kette ab, von dem der aktuelle Socket in Bezug auf PNP abhängig ist.                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**Wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
