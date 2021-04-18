---
title: Bluetooth-Programmierung mit Windows Sockets
description: In diesem Abschnitt wird beschrieben, wie Sie mit Windows Sockets-Funktionen und-Strukturen eine Bluetooth-Anwendung programmieren.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, Tasks
- Windows-Sockets
- Programmieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341721"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth-Programmierung mit Windows Sockets

In diesem Abschnitt wird beschrieben, wie Sie mit Windows Sockets-Funktionen und-Strukturen eine Bluetooth-Anwendung programmieren. Umfassende Referenzinformationen zu den Elementen der Windows Sockets-API finden Sie unter [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2). in diesem Abschnitt werden nur Bluetooth-spezifische Informationen für jedes Windows Sockets-Programmier Element bereitstellt.

Sie können auch das [Bluetooth-Verbindungs](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) Beispiel herunterladen, um ein umfassendes Beispiel zu erhalten.

Wie bei allen Windows Sockets-Anwendungsprogrammierung muss die [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion aufgerufen werden, um die Windows Sockets-Funktionalität zu initiieren und Bluetooth zu aktivieren.

Die folgenden Themen enthalten Anleitungen zur Verwendung von Windows Sockets-Funktionen und-Strukturen mit der Microsoft Bluetooth-API:



| Thema                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth und Accept](bluetooth-and-accept.md)                                                 | Bluetooth verwendet die [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Funktion, um eingehende Verbindungsversuche für einen Socket zu aktivieren.<br/>                                                                                                                                                                                                  |
| [Bluetooth und BIND](bluetooth-and-bind.md)                                                     | Bluetooth verwendet die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion, um eine Bindung an einen Socket herzustellen.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth und BLOB](bluetooth-and-blob.md)                                                     | Bluetooth verwendet die [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Struktur, um bei Aufrufen der [**wsasetservice**](bluetooth-and-wsasetservice.md) -oder **WSALookupService** -Funktionen Transport spezifische Daten an die [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur zu übergeben oder zu empfangen \* . <br/>             |
| [Bluetooth und Verbindung](bluetooth-and-connect.md)                                               | Bluetooth verwendet die [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktion zum Herstellen einer Verbindung mit einem Bluetooth-Ziel Gerät mithilfe eines zuvor erstellten Bluetooth-Sockets.<br/>                                                                                                                                                              |
| [Bluetooth und getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | Die [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion ermöglicht die Übersetzung von Hostnamen in Adressen für IP-basierte Transporte.<br/>                                                                                                                                                                                   |
| [Bluetooth und getPeer Name](bluetooth-and-getpeername.md)                                       | Dient zum Abrufen der Bluetooth-Adresse des Peer-Bluetooth-Geräts.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth und getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth Ruft mithilfe der Funktion [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) die Server Geräteadresse und die Portnummer ab, die einem Socket durch einen vorherigen Aufrufen der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion zugeordnet sind.<br/>                                                                                            |
| [Bluetooth und getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth verwendet die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, um verschiedene Parameter abzufragen, die dem Serverchannel oder der Verbindung zugeordnet sind. <br/>                                                                                                                                                           |
| [Bluetooth und lauschen, SELECT und closesocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth verwendet die Funktionen " [**lauschen**](/windows/desktop/api/winsock2/nf-winsock2-listen)", " [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)" und " [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) " ohne Änderungen der standardmäßigen Windows-Socketprogrammierung.<br/>                                                                                                   |
| [Bluetooth-und Lese-oder Schreibvorgänge](bluetooth-and-read-or-write-operations.md)             | Erläutert die unterstützten Winsock-Lese-und-Schreibvorgänge.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth und setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth verwendet die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, um verschiedene Parameter festzulegen, die dem Serverchannel oder der Verbindung zugeordnet sind.<br/>                                                                                                                                                              |
| [Bluetooth und Herunterfahren](bluetooth-and-shutdown.md)                                             | Bluetooth verwendet die Funktion zum [**herunter**](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren, um die Verbindung mit dem Remote Radio zu trennen.<br/>                                                                                                                                                                                                             |
| [Bluetooth und Socket](bluetooth-and-socket.md)                                                 | Bluetooth verwendet die [**Socketfunktion**](/windows/desktop/api/winsock2/nf-winsock2-socket) und erstellt einen Socket für eingehende oder ausgehende Verbindungen.<br/>                                                                                                                                                                                               |
| [Bluetooth-und Socket-Optionen](bluetooth-and-socket-options.md)                                 | Erläutert die Socketoptionen, die von Microsoft Bluetooth unterstützt werden.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth und wsaadresssstostring](bluetooth-and-wsaaddresstostring.md)                         | Wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion über die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur zur Verfügung gestellt wird, wenn Geräte Dienst Informationen abgerufen werden.<br/>                                           |
| [Bluetooth und wsalookupservicebegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth verwendet die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion zum Abfragen von Geräten und zum Ermitteln von Diensten.<br/>                                                                                                                                                                         |
| [Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth verwendet die [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zum Abgleichen von Abfragen, die in einem vorherigen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)-Befehl angegeben wurden.<br/>                                                                                                           |
| [Bluetooth und WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth verwendet die [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) -Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)initiiert wurde, und möglicherweise in nachfolgenden Aufrufen von [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)erweitert wurde.<br/> |
| [Bluetooth und wsaqueryset](bluetooth-and-wsaqueryset.md)                                       | Die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur wird in Vorgängen verwendet, einschließlich der Geräte Anfrage, der Dienst Anfrage und der Festlegung des Dienstanbieter.<br/>                                                                                                                                                                |
| [Bluetooth und wsasetservice](bluetooth-and-wsasetservice.md)                                   | Bluetooth verwendet die [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion, um eine Dienst Instanz im Bluetooth-Namespace (NS \_ BTH) aus der Registrierung zu registrieren oder zu entfernen.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

