---
description: Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Windows Sockets-Programmierung.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Einstieg in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43751663a637fafb2eec453a48c329ff8e4499f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359830"
---
# <a name="getting-started-with-winsock"></a>Einstieg in Winsock

Im folgenden finden Sie eine Schritt-für-Schritt-Anleitung für den Einstieg in die Windows Sockets-Programmierung. Es wurde entwickelt, um ein Verständnis der grundlegenden Winsock-Funktionen und-Datenstrukturen und deren Zusammenarbeit zu ermöglichen.

Die Client-und Serveranwendung, die zur Veranschaulichung verwendet wird, ist ein sehr grundlegender Client und Server. Erweiterte Codebeispiele sind in den im Microsoft Windows Software Development Kit (SDK) enthaltenen Beispielen enthalten.

Die ersten Schritte sind für Client-und Server Anwendungen identisch.

-   [Informationen zu Servern und Clients](about-clients-and-servers.md)
-   [Erstellen einer grundlegenden Winsock-Anwendung](creating-a-basic-winsock-application.md)
-   [Initialisieren von Winsock](initializing-winsock.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen einer WinSock-Client Anwendung beschrieben.

-   [Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)
-   [Herstellen einer Verbindung mit einem Socket](connecting-to-a-socket.md)
-   [Senden und empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)
-   [Trennen der Verbindung des Clients](disconnecting-the-client.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen einer Winsock-Serveranwendung beschrieben.

-   [Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)
-   [Binden eines Sockets](binding-a-socket.md)
-   [Lauschen an einem Socket](listening-on-a-socket.md)
-   [Akzeptieren einer Verbindung](accepting-a-connection.md)
-   [Empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)
-   [Trennen der Verbindung mit dem Server](disconnecting-the-server.md)

Der gesamte Quellcode für diese grundlegenden Beispiele.

-   [Ausführen des WinSock-Client-und Server Code Beispiels](finished-server-and-client-code.md)
-   [Vervollständigen des WinSock-Client Codes](complete-client-code.md)
-   [Vervollständigen des Winsock-Server Codes](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Erweiterte Winsock-Beispiele

Im Windows SDK sind mehrere erweiterte WinSock-Client-und Server Beispiele enthalten. Standardmäßig wird der Winsock-Beispiel Quell Code von der Windows SDK für Windows 7 im folgenden Verzeichnis installiert:

*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ Winsock*

In früheren Versionen der Windows SDK würde sich die Versionsnummer im obigen Pfad ändern. Der Winsock-Beispiel Quellcode wird z. b. vom Windows SDK für Windows Vista im folgenden Standardverzeichnis installiert.

*C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 6.0 \\ Beispiele \\ netds \\ Winsock*

Die weiter unten aufgeführten erweiterten Beispiele sind in den folgenden Verzeichnissen enthalten, um eine höhere Leistung zu erzielen:

-   IOCP

    Dieses Verzeichnis enthält drei Beispiel Programme, die e/a-Abschlussports verwenden. Die Programme enthalten einen Winsock-Server (iocpserver), der die [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion verwendet, einen Winsock-Server (iocpserverex), der die Funktion " [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) " verwendet, und einen einfachen Multithread-WinSock-Client (iocpclient), der zum Testen eines dieser Server verwendet wird. Die Serverprogramme unterstützen mehrere Clients, die eine Verbindung über TCP/IP herstellen und beliebige Datenpuffer senden, die vom Server an den Client zurückgesendet werden. Zur einfacheren Verwendung wurde ein einfaches Client Programm (iocpclient) entwickelt, um eine Verbindung herzustellen und Daten kontinuierlich an den Server zu senden, um Sie mit mehreren Threads zu belasten. Winsock-Server, die e/a-Abschlussports verwenden, bieten die größte Leistungsfähigkeit.

-   überlappen

    Dieses Verzeichnis enthält ein Beispiel Serverprogramm, das überlappende e/a-Vorgänge verwendet. Das Beispielprogramm verwendet die [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion und überlappende e/a-Vorgänge zur effektiven Verarbeitung mehrerer asynchroner Verbindungsanforderungen von Clients. Der Server verwendet die **Accept tex** -Funktion, um verschiedene Clientverbindungen in einer Single Thread-Win32-Anwendung zu multiplezieren. Die Verwendung von überlappenden e/a-Vorgängen ermöglicht eine größere Skalierbarkeit.

-   Wsapoll

    Dieses Verzeichnis enthält ein einfaches Beispielprogramm, das die Verwendung der [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktion veranschaulicht. Das kombinierte Client-und Serverprogramm ist nicht blockierend und verwendet die **wsapoll** -Funktion, um zu bestimmen, wann es möglich ist, ohne Blockierung zu senden oder zu empfangen. Dieses Beispiel dient zur Veranschaulichung und ist kein Hochleistungsserver.

-   Einfach

    Dieses Verzeichnis enthält drei grundlegende Beispiel Programme, die die Verwendung mehrerer Threads durch einen-Server veranschaulichen. Die Programme enthalten einen einfachen TCP/UDP-Server (simples), einen reinen TCP-Server (simples \_ IOCTL), der die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion in einer Win32-Konsolenanwendung verwendet, um mehrere Client Anforderungen zu unterstützen, und ein TCP/UDP-Client Programm (simplec) zum Testen der Server. Die Server veranschaulichen die Verwendung mehrerer Threads zum Verarbeiten mehrerer Client Anforderungen. Diese Methode hat Skalierbarkeits Probleme, da für jede Client Anforderung ein separater Thread erstellt wird.

-   accept (Akzeptieren)

    Dieses Verzeichnis enthält einen einfachen Beispiel Server und ein einfaches Client Programm. Der Server veranschaulicht die Verwendung der nicht blockierenden Annahme mithilfe der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion oder der asynchronen Annahme mithilfe der [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion. Dieses Beispiel dient zur Veranschaulichung und ist kein Hochleistungsserver.

 

 
