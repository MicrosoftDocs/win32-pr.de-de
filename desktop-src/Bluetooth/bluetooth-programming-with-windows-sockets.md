---
title: Bluetooth Programmieren mit Windows Sockets
description: In diesem Abschnitt wird beschrieben, wie Sie Windows Sockets-Funktionen und -Strukturen verwenden, um eine Bluetooth programmieren.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, Aufgaben
- Windows-Sockets
- Programmieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004090"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth Programmieren mit Windows Sockets

In diesem Abschnitt wird beschrieben, wie Sie Windows Sockets-Funktionen und -Strukturen verwenden, um eine Bluetooth programmieren. Vollständige Referenzinformationen für die Windows Sockets-API-Elemente finden Sie unter [Windows Sockets;](/windows/desktop/WinSock/windows-sockets-start-page-2) Dieser Abschnitt enthält nur Bluetooth spezifische Informationen für jedes Windows Sockets-Programmierelement.

Sie können auch das Beispiel Bluetooth [Verbindung herunterladen,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) um ein vollständiges Beispiel zu erhalten.

Wie bei allen Windows Sockets-Anwendungsprogrammierung muss die [**WSAStartup-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsastartup) aufgerufen werden, um Windows Sockets-Funktionalität zu initiieren und Bluetooth.

Die folgenden Themen enthalten Anleitungen zur Verwendung Windows Sockets-Funktionen und -Strukturen mit der Microsoft Bluetooth-API:



| Thema                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth und Akzeptieren](bluetooth-and-accept.md)                                                 | Bluetooth verwendet die [**accept-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-accept) um eingehende Verbindungsversuche für einen Socket zu aktivieren.<br/>                                                                                                                                                                                                  |
| [Bluetooth und Binden](bluetooth-and-bind.md)                                                     | Bluetooth verwendet die [**bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) zum Binden an einen Socket.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth und BLOB](bluetooth-and-blob.md)                                                     | Bluetooth verwendet die [](/windows/desktop/api/nspapi/ns-nspapi-blob) BLOB-Struktur, um transportspezifische Daten bei Aufrufen der [**WSASetService-**](bluetooth-and-wsasetservice.md) oder **WSALookupService-Funktionen** an die [**WSAQUERYSET-Struktur**](bluetooth-and-wsaqueryset-for-set-service.md) zu übergeben oder zu \* empfangen. <br/>             |
| [Bluetooth und Herstellen einer Verbindung](bluetooth-and-connect.md)                                               | Bluetooth verwendet die [**connect-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-connect) um eine Verbindung mit einem Zielgerät Bluetooth, indem ein zuvor erstellter Bluetooth wird.<br/>                                                                                                                                                              |
| [Bluetooth und getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | Die [**getaddrinfo-Funktion**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) ermöglicht die Übersetzung von Hostname zu Adresse für IP-basierte Transporte.<br/>                                                                                                                                                                                   |
| [Bluetooth und getpeername](bluetooth-and-getpeername.md)                                       | Wird zum Abrufen der Bluetooth-Adresse des Peer-Bluetooth verwendet.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth und getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth ruft mit der [**getsockname-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockname) die Servergeräteadresse und die Portnummer ab, die einem Socket durch einen vorherigen Aufruf der [**bind-Funktion zugeordnet**](/windows/desktop/api/winsock/nf-winsock-bind) wurden.<br/>                                                                                            |
| [Bluetooth und getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth verwendet die [**getsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) um verschiedene Parameter abfragt, die dem Serverkanal oder der Verbindung zugeordnet sind. <br/>                                                                                                                                                           |
| [Bluetooth und lauschen, auswählen und schließenOcket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth die Funktionen [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)und [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) verwendet, ohne dass änderungen an der Windows Sockets-Programmierung vorgenommen werden.<br/>                                                                                                   |
| [Bluetooth und Lese- oder Schreibvorgänge](bluetooth-and-read-or-write-operations.md)             | Hier finden Sie Details zu den unterstützten Winsock-Lese- und -Schreibvorgängen.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth und setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth verwendet die [**setsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-setsockopt) um verschiedene Parameter für den Serverkanal oder die Verbindung zu festlegen.<br/>                                                                                                                                                              |
| [Bluetooth und Herunterfahren](bluetooth-and-shutdown.md)                                             | Bluetooth verwendet die [**Funktion zum Herunterfahren,**](/windows/desktop/api/winsock/nf-winsock-shutdown) um die Verbindung mit dem Remoteschalter zu trennen.<br/>                                                                                                                                                                                                             |
| [Bluetooth und Socket](bluetooth-and-socket.md)                                                 | Bluetooth die [**Socketfunktion**](/windows/desktop/api/winsock2/nf-winsock2-socket) verwendet, erstellt einen Socket für eingehende oder ausgehende Verbindungen.<br/>                                                                                                                                                                                               |
| [Bluetooth und Socketoptionen](bluetooth-and-socket-options.md)                                 | Hier finden Sie Informationen zu den socket-Optionen, die von Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth und WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum für die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) über die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) beim Abrufen von Gerätedienstinformationen bereitgestellt wird.<br/>                                           |
| [Bluetooth und WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth verwendet die [**WSALookupServiceBegin-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) um Geräte abfragt und Dienste zu entdecken.<br/>                                                                                                                                                                         |
| [Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth verwendet die [**WSALookupServiceNext-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) um Abfragen zu erfüllen, die in einem vorherigen Aufruf von [**WSALookupServiceBegin angegeben wurden.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)<br/>                                                                                                           |
| [Bluetooth und WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth verwendet die [**WSALookupServiceEnd-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) um eine Abfrage zu beenden, die in einem vorherigen Aufruf von [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)initiiert wurde, und wurde möglicherweise in nachfolgenden Aufrufen von [**WSALookupServiceNext erweitert.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)<br/> |
| [Bluetooth und WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | Die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) wird in Vorgängen wie Geräteabfragen, Dienstabfragen und Festlegen des Diensts verwendet.<br/>                                                                                                                                                                |
| [Bluetooth und WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth verwendet die [**WSASetService-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) um eine Dienstinstanz im Bluetooth-Namespace (NS BTH) in der \_ Registrierung zu registrieren oder zu entfernen.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

