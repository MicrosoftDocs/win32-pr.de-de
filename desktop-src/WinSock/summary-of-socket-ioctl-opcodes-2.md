---
description: Einige der Socket-IOCTL-Opcodes für Windows Sockets 2 sind in der folgenden Tabelle zusammengefasst.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Zusammenfassung der Socket-Ioctl-Opcodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559660"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Zusammenfassung der Socket-Ioctl-Opcodes

Einige der Socket-IOCTL-Opcodes für Windows Sockets 2 sind in der folgenden Tabelle zusammengefasst. Ausführlichere Informationen finden Sie in der Winsock-Referenz zu [**Winsock IOCTLs**](winsock-ioctls.md) und der [**WSPIoctl-Funktion.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) Es gibt weitere neue protokollspezifische IOCTL-Opcodes, die im protokollspezifischen Anhang zu finden sind.

Eine vollständige Liste der [**Winsock-IOCTLs**](winsock-ioctls.md) finden Sie in der Winsock-Referenz.



| Opcode                                                      | Eingabetyp                               | Ausgabetyp                                 | Bedeutung                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Unsigned long                            | <Not used>                            | Aktiviert oder deaktiviert den Nichtblockierungsmodus für den Socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Unsigned long                               | Bestimmt die Menge der Daten, die atomisch aus dem Socket gelesen werden können.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Bestimmt, ob alle OOB-Daten gelesen wurden.                                                                                                                                                              |
| SIO \_ ASSOCIATE \_ HANDLE                                      | Abhängige Begleit-API                  | <Not used>                            | Ordnet den Socket dem angegebenen Handle einer Begleitschnittstelle zu.                                                                                                                                          |
| SIO ENABLE \_ CIRCULAR QUEUEING (SIO: AKTIVIEREN DER \_ \_ ZIRKULÄREN WARTESCHLANGE)                             | <Not used>                         | <Not used>                            | Aktiviert kreisförmiges Queuing.                                                                                                                                                                                          |
| SIO \_ FIND \_ ROUTE                                            | [**sockaddr-Struktur**](sockaddr-2.md) | <Not used>                            | Fordert die Route an die angegebene Adresse an, die gefunden werden soll.                                                                                                                                                      |
| SIO \_ FLUSH                                                  | <Not used>                         | <Not used>                            | Verwirft den aktuellen Inhalt der sendenden Warteschlange.                                                                                                                                                                    |
| SIO \_ GET \_ BROADCAST \_ ADDRESS                                | <Not used>                         | [**sockaddr-Struktur**](sockaddr-2.md)    | Ruft die protokollspezifische Broadcastadresse ab, die in [**WSPSendTo verwendet werden soll.**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                                                                                                                  |
| SIO \_ GET \_ QOS                                               | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Ruft die aktuellen Flussspezifikationen für den Socket ab.                                                                                                                                                              |
| SIO \_ GET \_ GROUP \_ QOS                                        | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Reserviert.                                                                                                                                                                                                          |
| SIO \_ MULTIPOINT \_ LOOPBACK                                   | BOOL                                     | <Not used>                            | Steuert, ob daten, die in einer Multipointsitzung gesendet werden, auch vom gleichen Socket auf dem lokalen Host empfangen werden.                                                                                                     |
| \_SIO-MULTICASTBEREICH \_                                       | INT                                      | <Not used>                            | Gibt den Bereich an, über den Multicastübertragungen erfolgen.                                                                                                                                                 |
| SIO \_ SET \_ QOS                                               | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Legt neue Flussspezifikationen für den Socket fest.                                                                                                                                                                |
| SIO \_ SET \_ GROUP \_ QOS                                        | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Reserviert.                                                                                                                                                                                                          |
| SIO \_ TRANSLATE \_ HANDLE                                      | INT                                      | Abhängige Begleit-API                     | Erhält ein entsprechendes Handle für *Sockets,* das im Kontext einer Begleitschnittstelle gültig ist.                                                                                                               |
| ABFRAGE DER \_ \_ SIO-ROUTINGSCHNITTSTELLE \_                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Erhält die Adresse der lokalen Schnittstelle, die zum Senden an die angegebene Adresse verwendet werden soll.                                                                                                                   |
| \_ \_ SIO-ROUTINGSCHNITTSTELLENÄNDERUNG \_                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Fordert eine Benachrichtigung über Änderungen an Informationen an, die über SIO \_ ROUTING INTERFACE QUERY für die angegebene Adresse gemeldet \_ \_ werden.                                                                                         |
| [**ABFRAGE DER \_ \_ SIO-ADRESSLISTE \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**\_SOCKETADRESSE**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Erhält eine Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann. Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen. |
| ÄNDERUNG DER \_ \_ SIO-ADRESSLISTE \_                                  | <Not used>                         | <Not used>                            | Fordert eine Benachrichtigung über Änderungen an Informationen an, die über SIO \_ ADDRESS LIST QUERY gemeldet \_ \_ werden.                                                                                                                         |
| SIO \_ QUERY \_ PNP \_ TARGET \_ HANDLE                             | <Not used>                         | Socket                                      | Erhält den Socketdeskriptor des nächsten Anbieters in der Kette, von der der aktuelle Socket in Bezug auf PnP abhängt.                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Winsock-IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
