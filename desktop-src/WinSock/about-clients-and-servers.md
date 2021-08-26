---
description: 'Es gibt zwei verschiedene Arten von Socketnetzwerkanwendungen: Server und Client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informationen zu Servern und Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d8016d1fc9c23b901a03a924cd0e3ade3982dc2e1bf0db277eac47170d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898640"
---
# <a name="about-servers-and-clients"></a>Informationen zu Servern und Clients

Es gibt zwei verschiedene Arten von Socketnetzwerkanwendungen: Server und Client.

Server und Clients haben unterschiedliche Verhaltensweisen. Daher ist der Prozess der Erstellung unterschiedlich. Im Folgenden finden Sie das allgemeine Modell zum Erstellen eines TCP/IP-Streamingservers und -Clients.

## <a name="server"></a>Server

1.  Initialisieren Sie Winsock.
2.  Erstellen Sie einen Socket.
3.  Binden Sie den Socket.
4.  Lauschen Sie am Socket auf einen Client.
5.  Akzeptieren Sie eine Verbindung von einem Client.
6.  Empfangen und Senden von Daten.
7.  Trennen.

## <a name="client"></a>Client

1.  Initialisieren Sie Winsock.
2.  Erstellen Sie einen Socket.
3.  Stellen Sie eine Verbindung mit dem Server her.
4.  Senden und Empfangen von Daten.
5.  Trennen.

> [!Note]  
> Einige der Schritte sind für einen Client und einen Server identisch. Diese Schritte werden fast genau gleich implementiert. Einige der Schritte in diesem Leitfaden sind spezifisch für den Typ der anwendung, die erstellt wird.

 

Erster Schritt: [Erstellen einer einfachen Winsock-Anwendung](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



