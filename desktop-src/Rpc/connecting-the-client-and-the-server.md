---
title: Herstellen einer Verbindung zwischen Client und Server
description: Für die Kommunikation müssen Client- und Serverprogramme eine Kommunikationssitzung über das Netzwerk oder netzwerke hinweg einrichten, die sie verbinden.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Remoteprozeduraufruf RPC , Tasks, Verbinden von Client und Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f477802ffb4b72f33ce951bf811b1cb9b770a8272f646507dfaa450934569f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931227"
---
# <a name="connecting-the-client-and-the-server"></a>Herstellen einer Verbindung zwischen Client und Server

Für die Kommunikation müssen Client- und Serverprogramme eine Kommunikationssitzung über das Netzwerk oder netzwerke hinweg einrichten, die sie verbinden. Nachdem die Verbindung hergestellt wurde, kann der Client Remoteprozeduren im Serverprogramm aufrufen, als wären sie lokal im Clientprogramm.

Dieser Abschnitt bietet eine konzeptionelle Übersicht über das Herstellen einer Verbindung zwischen Clients und Servern für Remoteprozeduraufrufe. Sie bietet keine ausführliche Erläuterung dieses Themas. Alle Konzepte in diesem Abschnitt werden in späteren Kapiteln und im Abschnitt RPC-Funktionsreferenz ausführlich vorgestellt.

Die in diesem Abschnitt vorgestellte Diskussion ist in die folgenden Themen unterteilt:

-   [Grundlegende RPC-Bindungsterminologie](essential-rpc-binding-terminology.md)
-   [Vorbereiten einer Verbindung durch den Server](how-the-server-prepares-for-a-connection.md)
-   [Herstellen einer Verbindung durch den Client](how-the-client-establishes-a-connection.md)

Beachten Sie, dass bei der Diskussion explizite Bindungshandles angenommen werden. Wenn Ihre Anwendung jedoch andere Arten von Bindungshandles verwendet, müssen Sie möglicherweise die in diesem Abschnitt beschriebenen Schritte ändern. Weitere Informationen finden Sie unter [Bindung und Handles.](binding-and-handles.md)

 

 




