---
description: Im Folgenden finden Sie eine Schritt-für-Schritt-Anleitung für die ersten Schritte mit Windows Sockets-Programmierung.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Erste Schritte mit Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcce956d7dcb142e4a51ac3a461868dfa055acc9a2d1624b6a6dff5132f86ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132153"
---
# <a name="getting-started-with-winsock"></a>Erste Schritte mit Winsock

Im Folgenden finden Sie eine Schritt-für-Schritt-Anleitung für die ersten Schritte mit Windows Sockets-Programmierung. Es soll ein Verständnis der grundlegenden Winsock-Funktionen und Datenstrukturen sowie deren Zusammenarbeit bieten.

Die Client- und Serveranwendung, die zur Veranschaulichung verwendet wird, ist ein sehr grundlegender Client und Server. Erweiterte Codebeispiele sind in den Beispielen enthalten, die im Microsoft Windows Software Development Kit (SDK) enthalten sind.

Die ersten Schritte sind für Client- und Serveranwendungen identisch.

-   [Informationen zu Servern und Clients](about-clients-and-servers.md)
-   [Erstellen einer einfachen Winsock-Anwendung](creating-a-basic-winsock-application.md)
-   [Initialisieren von Winsock](initializing-winsock.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen einer Winsock-Clientanwendung beschrieben.

-   [Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)
-   [Herstellen einer Verbindung mit einem Socket](connecting-to-a-socket.md)
-   [Senden und Empfangen von Daten auf dem Client](sending-and-receiving-data-on-the-client.md)
-   [Trennen des Clients](disconnecting-the-client.md)

In den folgenden Abschnitten werden die verbleibenden Schritte zum Erstellen einer Winsock-Serveranwendung beschrieben.

-   [Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)
-   [Binden eines Sockets](binding-a-socket.md)
-   [Lauschen an einem Socket](listening-on-a-socket.md)
-   [Akzeptieren einer Verbindung](accepting-a-connection.md)
-   [Empfangen und Senden von Daten auf dem Server](receiving-and-sending-data-on-the-server.md)
-   [Trennen des Servers](disconnecting-the-server.md)

Der vollständige Quellcode für diese grundlegenden Beispiele.

-   [Ausführen des Winsock-Client- und -Servercodebeispiels](finished-server-and-client-code.md)
-   [Vollständigen Winsock-Clientcode](complete-client-code.md)
-   [Vollständigen Winsock-Servercode](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Erweiterte Winsock-Beispiele

Mehrere erweiterte Winsock-Client- und -Serverbeispiele sind im Windows SDK enthalten. Standardmäßig wird der Quellcode des Winsock-Beispiels im folgenden Verzeichnis vom Windows SDK für Windows 7 installiert:

*C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock*

In früheren Versionen des Windows SDK ändert sich die Versionsnummer im obigen Pfad. Der Quellcode des Winsock-Beispiels wird beispielsweise im folgenden Standardverzeichnis vom Windows SDK für Windows Vista installiert.

*C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Die weiter unten aufgeführten erweiterten Beispiele für höhere bis niedrigere Leistung finden Sie in den folgenden Verzeichnissen:

-   iocp

    Dieses Verzeichnis enthält drei Beispielprogramme, die E/A-Vervollständigungsports verwenden. Die Programme umfassen einen Winsock-Server (iocpserver), der die [**WSAAccept-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) verwendet, einen Winsock-Server (iocpserverex), der die [**AcceptEx-Funktion**](/windows/win32/api/mswsock/nf-mswsock-acceptex) verwendet, und einen einfachen Multithread-Winsock-Client (iocpclient), der zum Testen eines dieser Server verwendet wird. Die Serverprogramme unterstützen mehrere Clients, die über TCP/IP eine Verbindung herstellen und Datenpuffer beliebiger Größe senden, die der Server dann an den Client zurücksenden kann. Der Einfachheit halber wurde ein einfaches Clientprogramm, iocpclient, entwickelt, um eine Verbindung herzustellen und kontinuierlich Daten an den Server zu senden, um sie mithilfe mehrerer Threads zu beanspruchen. Winsock-Server, die E/A-Vervollständigungsports verwenden, bieten die meisten Leistungsfunktionen.

-   Überlappen

    Dieses Verzeichnis enthält ein Beispielserverprogramm, das überlappende E/A verwendet. Das Beispielprogramm verwendet die [**AcceptEx-Funktion**](/windows/win32/api/mswsock/nf-mswsock-acceptex) und überlappende E/A, um mehrere asynchrone Verbindungsanforderungen von Clients effektiv zu verarbeiten. Der Server verwendet die **AcceptEx-Funktion,** um verschiedene Clientverbindungen in einer Win32-Einzelthreadanwendung zu multiplexen. Die Verwendung überlappende E/A ermöglicht eine höhere Skalierbarkeit.

-   WSAPoll

    Dieses Verzeichnis enthält ein einfaches Beispielprogramm, das die Verwendung der [**WSAPoll-Funktion**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) veranschaulicht. Das kombinierte Client- und Serverprogramm ist nicht blockierend und verwendet die **WSAPoll-Funktion,** um zu bestimmen, wann das Senden oder Empfangen ohne Blockierung möglich ist. Dieses Beispiel ist eher zur Veranschaulichung und kein Hochleistungsserver.

-   Einfach

    Dieses Verzeichnis enthält drei grundlegende Beispielprogramme, die die Verwendung mehrerer Threads durch einen Server veranschaulichen. Die Programme umfassen einen einfachen TCP/UDP-Server (simples), einen server only TCP -Server (simples ioctl), der die select-Funktion in einer Win32-Konsolenanwendung verwendet, um mehrere Clientanforderungen zu unterstützen, und ein \_ TCP/UDP-Clientprogramm [](/windows/desktop/api/Winsock2/nf-winsock2-select) (simplec) zum Testen der Server. Die Server zeigen die Verwendung mehrerer Threads zur Handhabung mehrerer Clientanforderungen. Diese Methode hat Skalierbarkeitsprobleme, da für jede Clientanforderung ein separater Thread erstellt wird.

-   accept (Akzeptieren)

    Dieses Verzeichnis enthält einen einfachen Beispielserver und ein Clientprogramm. Der Server veranschaulicht die Verwendung der nicht blockierenden Annahme mithilfe der [**select-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-select) oder der asynchronen Annahme mithilfe der [**WSAAsyncSelect-Funktion.**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) Dieses Beispiel ist eher zur Veranschaulichung und kein Hochleistungsserver.

 

 
