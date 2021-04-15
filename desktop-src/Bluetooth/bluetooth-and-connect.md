---
title: Bluetooth und Verbindung
description: Bluetooth verwendet die Connect-Funktion zum Herstellen einer Verbindung mit einem Bluetooth-Ziel Gerät mithilfe eines zuvor erstellten Bluetooth-Sockets.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- Bluetooth verbinden
- Bluetooth und Verbinden von Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474061"
---
# <a name="bluetooth-and-connect"></a>Bluetooth und Verbindung

Bluetooth verwendet die [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion zum Herstellen einer Verbindung mit einem Bluetooth-Ziel Gerät mithilfe eines zuvor erstellten Bluetooth-Sockets. Der *Name* -Parameter der **Connect** -Funktion, bei der es sich um eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur handelt, muss ein Bluetooth-Ziel Gerät angeben. Es werden zwei Mechanismen verwendet, um das Zielgerät zu identifizieren:

-   Die [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur kann die Portnummer, an die eine Verbindung angefordert wird, direkt angeben. Dieser Mechanismus erfordert, dass die Anwendung eigene SDP-Abfragen ausführt, bevor versucht wird, einen [**Verbindungs**](/windows/desktop/api/winsock2/nf-winsock2-connect) Vorgang durchzuführen.
-   Die [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur kann die eindeutige Dienst Klassen-ID des dienstanzdienstanbieter angeben, mit dem eine Verbindung hergestellt werden soll. Wenn das peergerät über mehr als einen Port verfügt, der der Dienst Klassen-ID entspricht, stellt der Verbindungs Funktionsaufrufe eine [**Verbindung**](/windows/desktop/api/winsock2/nf-winsock2-connect) mit dem ersten gültigen Dienst her. Dieser Mechanismus kann ohne vorherige SDP-Abfragen verwendet werden.

Wenn Sie die [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur mit der [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion verwenden, gelten die folgenden Anforderungen:

-   Der **btaddr** -Member muss eine gültige Remote-Radio Adresse sein.
-   Wenn für den **serviceclassid-** Member der portmember NULL ist, versucht das System, **serviceclassid** zu verwenden, um den Remoteport aufzulösen, der dem Dienst entspricht. Die Dienstklasse ist eine normalisierte 128-Bit-GUID, die durch die Bluetooth-Spezifikation definiert wird. Allgemeine GUIDs werden durch das Dokument "Bluetooth Assigned Numbers" definiert. Alternativ kann eine eindeutige GUID für eine domänenspezifische Anwendung verwendet werden.
-   Der **portmember** muss ein gültiger Remoteport sein, oder 0 (null), wenn der **serviceclassid-** Member angegeben wird.

In der folgenden Tabelle werden die Ergebnis Codes für Bluetooth und die [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion aufgelistet.

| Fehler/Fehler\#                    | BESCHREIBUNG                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | Die [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion, die für den bereits verbundenen Socket aufgerufen wird. |
| WSAEACCES10013<br/>        | Die von der Anwendung angeforderte Authentifizierung wird verbunden        |
| WSAENOBUFS10055<br/>       | Nicht BEHEB barer Fehler wegen nicht BEHEB baren Arbeitsspeichers.                                                 |
| WSAEADDRINUSE10048<br/>    | Die angeforderte Port-/Channelnummer wird verwendet.                                       |
| WSAETIMEDOUT10060<br/>     | Das e/a-Timeout auf der Bluetooth-Options Ebene (Seiten \_ Timeout).                    |
| WSAEDISCON10101<br/>       | Der RFCOMM-Kanal wurde vom Remotepeer getrennt.                                    |
| WSAECONNRESET10054<br/>    | Das RFCOMM-Modul (Session) wurde vom Remotepeer getrennt.                      |
| WSAECONNABORTED10053<br/>  | Der Socket wurde von der Anwendung heruntergefahren.                                                   |
| WSAENETUNREACH10051<br/>   | Anderer Fehler als Timeout auf L2CAP-oder Bluetooth-Options Ebene.                       |
| WSAEHOSTDOWN10064<br/>     | Die RFCOMM hat DM-Antwort empfangen.                                                   |
| WSAENETDOWN10050<br/>      | Unerwarteter Netzwerkfehler.                                                          |
| WSAESHUTDOWN10058<br/>     | Der L2CAP-Kanal wurde vom Remotepeer getrennt.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Der Bluetooth-Port/-Kanal oder die Geräteadresse ist ungültig.                                |
| WSAEINVAL10022<br/>        | Der Plug & Play, das Treiber Stapel Ereignis oder ein anderer Fehler hat einen Fehler verursacht.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**herzustellen**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

