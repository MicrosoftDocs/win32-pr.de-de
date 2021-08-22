---
description: Ausführen des vollständigen BEISPIELcodes für TCP/IP-Client und Serveranwendung.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ausführen des Winsock-Client- und Servercodebeispiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb5a4b2385c9545410cfc29c913ea81660f6dc2810b92279fad22212781065c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132483"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Ausführen des Winsock-Client- und Servercodebeispiels

Dieser Abschnitt enthält den vollständigen Quellcode für die TCP/IP-Client- und Serveranwendungen:

-   [Abschließen des Winsock-Clientcodes](complete-client-code.md)
-   [Abschließen des Winsock-Servercodes](complete-server-code.md)

Die Serveranwendung sollte gestartet werden, bevor die Clientanwendung gestartet wird.

Kompilieren Sie zum Ausführen des Servers den vollständigen Serverquellcode, und führen Sie die ausführbare Datei aus. Die Serveranwendung lauscht an TCP-Port 27015, damit ein Client eine Verbindung herstellen kann. Sobald ein Client eine Verbindung herstellt, empfängt der Server Daten vom Client und gibt die empfangenen Daten an den Client zurück (sendet). Wenn der Client die Verbindung herunterfährt, fährt der Server den Clientsocket herunter, schließt den Socket und beendet den Socket.

Kompilieren Sie den vollständigen Clientquellcode, und führen Sie die ausführbare Datei aus, um den Client auszuführen. Die Clientanwendung erfordert, dass der Name des Computers oder der IP-Adresse des Computers, auf dem die Serveranwendung ausgeführt wird, als Befehlszeilenparameter übergeben wird, wenn der Client ausgeführt wird. Wenn der Client und der Server auf dem Beispielcomputer ausgeführt werden, kann der Client wie folgt gestartet werden:

**client localhost**

Der Client versucht, über TCP-Port 27015 eine Verbindung mit dem Server herzustellen. Sobald der Client eine Verbindung herstellt, sendet der Client Daten an den Server und empfängt alle Daten, die vom Server zurücksenden. Der Client schließt dann den Socket und wird beendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



