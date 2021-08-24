---
title: Bluetooth und Herstellen einer Verbindung
description: Bluetooth verwendet die Connect-Funktion, um eine Verbindung mit einem Zielgerät Bluetooth, indem ein zuvor erstellter Bluetooth wird.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- Verbinden Bluetooth
- Bluetooth und Verbinden Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588460"
---
# <a name="bluetooth-and-connect"></a>Bluetooth und Herstellen einer Verbindung

Bluetooth verwendet die [**connect-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-connect) um eine Verbindung mit einem Zielgerät Bluetooth, indem ein zuvor erstellter Bluetooth wird. Der *Name-Parameter* der **Connect-Funktion,** bei dem es sich um eine [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) handelt, muss ein Ziel für Bluetooth angeben. Zum Identifizieren des Zielgeräts werden zwei Mechanismen verwendet:

-   Die [**\_ SOCKADDR-BTH-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) kann direkt die Portnummer angeben, mit der eine Verbindung angefordert wird. Dieser Mechanismus erfordert, dass die Anwendung vor dem Versuch, eine Verbindung herzustellen, eigene [**SDP-Abfragen**](/windows/desktop/api/winsock2/nf-winsock2-connect) ausführen kann.
-   Die [**\_ SOCKADDR-BTH-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) kann die eindeutige Dienstklassen-ID des Diensts angeben, mit dem eine Verbindung hergestellt werden soll. Wenn das Peergerät über mehrere Ports verfügt, die [](/windows/desktop/api/winsock2/nf-winsock2-connect) der Dienstklassen-ID entsprechen, stellt der Connect-Funktionsaufruf eine Verbindung mit dem ersten gültigen Dienst herstellen. Dieser Mechanismus kann ohne vorherige SDP-Abfragen verwendet werden.

Wenn Sie die [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) mit der [**connect-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-connect) verwenden, gelten die folgenden Anforderungen:

-   Der **btAddr-Member** muss eine gültige Remote-Radioadresse sein.
-   Wenn das Portmitglied für das **serviceClassId-Mitglied** 0 (null) ist, versucht das System, **serviceClassId** zu verwenden, um den Remoteport aufzulösen, der dem Dienst entspricht. Die Dienstklasse ist eine normalisierte 128-Bit-GUID, die durch die Bluetooth definiert wird. Allgemeine GUIDs werden durch das Dokument Bluetooth Zugewiesene Zahlen definiert. Alternativ kann eine eindeutige GUID für eine domänenspezifische Anwendung verwendet werden.
-   Der **Port-Member** muss ein gültiger Remoteport oder 0 (null) sein, wenn **der serviceClassId-Member** angegeben ist.

In der folgenden Tabelle sind die Ergebniscodes für Bluetooth und die [**Connect-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-connect) aufgeführt.

| Fehler/Fehler\#                    | Beschreibung                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Die [**connect-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-connect) die für bereits verbundenen Socket aufgerufen wird. |
| WSAEACCES10013<br/>        | Beim Herstellen einer Verbindung mit der Anwendung wurde die Authentifizierung angefordert, aber die Authentifizierung ist fehlgeschlagen.        |
| WSAENOBUFS10055<br/>       | Nicht behebbarer Fehler mit nicht genügend Arbeitsspeicher.                                                 |
| WSAEADDRINUSE10048<br/>    | Die angeforderte Port-/Kanalnummer wird verwendet.                                       |
| WSAETIMEDOUT10060<br/>     | Für die E/A ist ein Timeout auf Bluetooth Radioebene (PAGE \_ TIMEOUT) erfolgt.                    |
| WSAEDISCON10101<br/>       | Der RFCOMM-Kanal, der vom Remote-Peer getrennt ist.                                    |
| WSAECONNRESET10054<br/>    | Der RFCOMM-Multiplexor (Sitzung), der durch einen Remote-Peer getrennt ist.                      |
| WSAECONNABORTED10053<br/>  | Der Socket wird von der Anwendung heruntergefahren.                                                   |
| WSAENETUNREACH10051<br/>   | Ein anderer Fehler als time-out auf L2CAP- oder Bluetooth-Ebene.                       |
| WSAEHOSTDOWN10064<br/>     | Der RFCOMM hat eine DM-Antwort empfangen.                                                   |
| WSAENETDOWN10050<br/>      | Unerwarteter Netzwerkfehler.                                                          |
| WSAESHUTDOWN10058<br/>     | Der L2CAP-Kanal, der vom Remote-Peer getrennt wurde.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Bluetooth Port/Kanal oder Geräteadresse ungültig.                                |
| WSAEINVAL10022<br/>        | Plug & Play, Treiberstapelereignis oder ein anderer Fehler hat einen Fehler verursacht.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Verbinden**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

