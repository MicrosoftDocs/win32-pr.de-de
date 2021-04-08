---
title: Auswählen einer Protokoll Sequenz
description: Eine Protokoll Sequenz ist die Sprache, die ein Netzwerk Betriebssystem verwendet, um über das Netzwerk mit anderen Computern zu kommunizieren.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037414"
---
# <a name="selecting-a-protocol-sequence"></a>Auswählen einer Protokoll Sequenz

Eine Protokoll Sequenz ist die Sprache, die ein Netzwerk Betriebssystem verwendet, um über das Netzwerk mit anderen Computern zu kommunizieren. In spezifischeren Begriffen müssen RPC-Anwendungen eine Zeichenfolge angeben, die eine Kombination aus einem RPC-Protokoll, einem Transportprotokoll und einem Netzwerkprotokoll darstellt.

Microsoft RPC unterstützt drei RPC-Protokolle:

-   Verbindungs orientiertes Protokoll der Netzwerk Rechen Architektur (ncacn)
-   Network Computing Architecture Datagram Protocol (ncadg)
-   Lokaler Remote Prozedur Aufruf (Ncalrpc) für die Netzwerk Computing-Architektur

RPC-Anwendungen können das Ncalrpc-Protokoll verwenden, um Prozeduren von Serverprogrammen aufzurufen, die auf demselben Computer ausgeführt werden, auf dem das Client Programm ausgeführt wird. Dies ist bisher die effizienteste Methode zum Aufrufen von Funktionen in einem anderen Prozess auf demselben Computer.

Welche Transport-und Netzwerkprotokolle von Ihrer Anwendung verwendet werden, hängt davon ab, welche Protokolle das Netzwerk unterstützt. Viele Netzwerke, einschließlich des Internets, unterstützen TCP/IP. Andere gängige Transport-und Netzwerkprotokolle sind IPX/SPX, NetBIOS und AppleTalk DSP. Microsoft RPC unterstützt diese und andere Transport-und Netzwerkprotokolle. Eine komplette Liste finden Sie unter [Protokoll Sequenz Konstanten](protocol-sequence-constants.md).

Wenn Ihre Anwendung automatische Bindungs Handles verwendet, muss Sie die Protokoll Sequenz nicht angeben. Wenn Sie implizite oder explizite Handles verwendet, muss Sie die Protokoll Sequenz abrufen oder angeben. Jedes verteilte System muss die Umgebung untersuchen, in der es bereitgestellt wird, um zu bestimmen, welche Protokoll Sequenz für diese Umgebung am besten geeignet ist.

Nicht alle Protokoll Sequenzen verfügen über äquivalente Funktionalität. Entwickler sollten überprüfen, ob die ausgewählte Protokoll Sequenz die erforderlichen Features unterstützt. Im Allgemeinen werden **Ncalrpc** für die lokale Kommunikation und **ncacn \_ IP \_ TCP** oder **ncacn \_ http** for Remote Communications empfohlen. Sie funktionieren in allen Umgebungen, haben eine optimale Leistung und unterstützen alle notwendigen, bewährten Features.

Clients können auch Protokoll Sequenz Informationen angeben, die Sie von Active Directory, die Registrierung, die vom Setup Programm erstellten und initialisierten Umgebungsvariablen, anwendungsspezifische Konfigurationsdateien oder Literalzeichenfolgen im Quellcode des Programms erhalten.

Nachdem das Client Programm eine gültige Protokoll Sequenz Zeichenfolge aufweist, kann es diese Informationen an die Funktionen [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) und [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) übergeben, um das Bindungs Handle zu erstellen.

 

 




