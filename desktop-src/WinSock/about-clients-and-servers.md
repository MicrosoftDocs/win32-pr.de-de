---
description: 'Es gibt zwei unterschiedliche Arten von socketnetzwerkanwendungen: Server und Client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informationen zu Servern und Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353072"
---
# <a name="about-servers-and-clients"></a>Informationen zu Servern und Clients

Es gibt zwei unterschiedliche Arten von socketnetzwerkanwendungen: Server und Client.

Server und Clients haben unterschiedliche Verhaltensweisen. Daher ist der Prozess der Erstellung anders. Im folgenden finden Sie das allgemeine Modell zum Erstellen eines TCP/IP-Streamingservers und-Clients.

## <a name="server"></a>Server

1.  Initialisieren Sie Winsock.
2.  Erstellen Sie einen Socket.
3.  Binden Sie den Socket.
4.  Lauschen Sie an den Socket für einen Client.
5.  Akzeptieren Sie eine Verbindung von einem Client.
6.  Empfangen und Senden von Daten.
7.  Trennen.

## <a name="client"></a>Client

1.  Initialisieren Sie Winsock.
2.  Erstellen Sie einen Socket.
3.  Stellen Sie eine Verbindung mit dem Server her.
4.  Senden und empfangen von Daten.
5.  Trennen.

> [!Note]  
> Einige der Schritte sind für einen Client und einen Server identisch. Diese Schritte sind nahezu genau gleichermaßen implementiert. Einige der Schritte in diesem Handbuch gelten speziell für den Typ der Anwendung, die erstellt wird.

 

Erster Schritt: [Erstellen einer grundlegenden Winsock-Anwendung](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einstieg in Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



