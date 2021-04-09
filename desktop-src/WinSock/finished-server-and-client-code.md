---
description: Der gesamte Beispielcode für die TCP/IP-Client-und-Serveranwendung wird ausgeführt.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ausführen des WinSock-Client-und Server Code Beispiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958929"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Ausführen des WinSock-Client-und Server Code Beispiels

Dieser Abschnitt enthält den gesamten Quellcode für die TCP/IP-Client-und-Server Anwendungen:

-   [Vervollständigen des WinSock-Client Codes](complete-client-code.md)
-   [Vervollständigen des Winsock-Server Codes](complete-server-code.md)

Die Serveranwendung muss gestartet werden, bevor die Client Anwendung gestartet wird.

Kompilieren Sie zum Ausführen des Servers den vollständigen Server Quellcode, und führen Sie die ausführbare Datei aus. Die Serveranwendung lauscht an TCP-Port 27015, wenn ein Client eine Verbindung herstellen soll. Nachdem ein Client eine Verbindung hergestellt hat, empfängt der Server die Daten vom Client und gibt die Daten zurück, die an den Client zurückgesendet werden. Wenn der Client die Verbindung herunterfährt, fährt der Server den Clientsocket herunter, schließt den Socket und wird beendet.

Kompilieren Sie den vollständigen Client Quellcode, und führen Sie die ausführbare Datei aus, um den Client auszuführen. Die Client Anwendung erfordert, dass der Name des Computers oder der IP-Adresse des Computers, auf dem die Serveranwendung ausgeführt wird, als Befehlszeilenparameter übergeben wird, wenn der Client ausgeführt wird. Wenn der Client und der Server auf dem Beispiel Computer ausgeführt werden, kann der Client wie folgt gestartet werden:

**Client localhost**

Der Client versucht, eine Verbindung mit dem Server über den TCP-Port 27015 herzustellen. Sobald der Client eine Verbindung herstellt, sendet der Client Daten an den Server und empfängt alle vom Server zurückgesendeten Daten. Der Client schließt dann den Socket und wird beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



