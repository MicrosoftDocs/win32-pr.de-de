---
title: Verbinden des Clients und des Servers
description: Zur Kommunikation müssen Client-und Serverprogramme eine Kommunikationssitzung im Netzwerk oder in Netzwerken einrichten, die Sie miteinander verbinden.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verbinden von Client und Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471389"
---
# <a name="connecting-the-client-and-the-server"></a>Verbinden des Clients und des Servers

Zur Kommunikation müssen Client-und Serverprogramme eine Kommunikationssitzung im Netzwerk oder in Netzwerken einrichten, die Sie miteinander verbinden. Nachdem Sie die Verbindung hergestellt haben, kann der Client Remote Prozeduren im Serverprogramm so abrufen, als wären Sie lokal für das Client Programm.

Dieser Abschnitt enthält eine konzeptionelle Übersicht über das Herstellen einer Verbindung zwischen Clients und Servern für Remote Prozedur Aufrufe. Es wird keine ausführliche Erörterung dieses Themas bereitgestellt. Alle Konzepte in diesem Abschnitt werden in späteren Kapiteln und im Abschnitt zur RPC-Funktionsreferenz ausführlich dargestellt.

Die in diesem Abschnitt gezeigte Diskussion ist in die folgenden Themen unterteilt:

-   [Wichtige RPC-Bindungs Terminologie](essential-rpc-binding-terminology.md)
-   [Wie der Server eine Verbindung vorbereitet](how-the-server-prepares-for-a-connection.md)
-   [Einrichten einer Verbindung durch den Client](how-the-client-establishes-a-connection.md)

Beachten Sie, dass die Diskussion explizite Bindungs Handles annimmt. Wenn Ihre Anwendung jedoch andere Typen von Bindungs Handles verwendet, müssen Sie möglicherweise die in diesem Abschnitt beschriebenen Schritte ändern. Weitere Informationen finden Sie unter [Bindung und Handles](binding-and-handles.md).

 

 




