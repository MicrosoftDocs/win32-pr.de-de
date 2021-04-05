---
title: Einrichten einer Verbindung durch den Client
description: Um eine Client/Server-Kommunikationssitzung mit einem Serverprogramm einzurichten, müssen Client Anwendungen mit expliziten Handles ein Bindungs Handle erstellen.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037079"
---
# <a name="how-the-client-establishes-a-connection"></a>Einrichten einer Verbindung durch den Client

Um eine Client/Server-Kommunikationssitzung mit einem Serverprogramm einzurichten, müssen Client Anwendungen mit expliziten Handles ein Bindungs Handle erstellen. Danach findet die RPC-Lauf Zeit Bibliothek den Computer, der das Serverprogramm hostet. Anschließend findet der Endpunkt den Endpunkt, an dem das Serverprogramm lauscht, und leitet ihn an ihn weiter. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![ein RPC-Client stellt eine Verbindung mit einem RPC-Server her.](images/clntcon.png)

Dieser Abschnitt enthält Informationen darüber, wie der Client eine Verbindung mit dem Serverprogramm herstellt und die von ihm angebotenen Remote Prozeduren ausführt. Es gibt viele Ansätze für die Ausführung dieser Schritte. je nach ausgewähltem Entwurf kann eine Anwendung eine andere Gruppe von Schritten auswählen. Dieses Beispiel ist einfach eine Möglichkeit.

Die Diskussion ist in die folgenden Abschnitte unterteilt:

-   [Erstellen eines Bindungs Handles](creating-a-binding-handle.md)
-   [Ausführen eines Remote Prozedur Aufrufes](making-a-remote-procedure-call.md)
-   [Suchen des Server Programms](finding-the-server-program.md)
-   [Senden des Aufrufes an das Server Programm](sending-the-call-to-the-server-program.md)

 

 




