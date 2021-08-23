---
description: Der Systemereignisbenachrichtigungsdienst ermöglicht mobilen Anwendungen den Empfang von Benachrichtigungen von Systemereignissen, die SENS überwacht. Wenn das angeforderte Ereignis auftritt, benachrichtigt SENS die Anwendung.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Benachrichtigungen (Systemereignisbenachrichtigungsdienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db908c48c38ccd39c6c9a427b77e3cefffc7b9bf8fad6e464ebdf146a138e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003968"
---
# <a name="notifications-system-event-notification-service"></a>Benachrichtigungen (Systemereignisbenachrichtigungsdienst)

Der Systemereignisbenachrichtigungsdienst ermöglicht mobilen Anwendungen den Empfang von Benachrichtigungen von Systemereignissen, die SENS überwacht. Wenn das angeforderte Ereignis auftritt, benachrichtigt SENS die Anwendung.

SENS kann Anwendungen über drei Klassen von Systemereignissen benachrichtigen:

-   TCP/IP-Netzwerkereignisse, z. B. der Status einer TCP/IP-Netzwerkverbindung oder die Qualität der Verbindung.
-   Benutzeranmeldungsereignisse.
-   Akku- und Wechselstromereignisse.

Beispielsweise kann eine Anwendung eines der folgenden Systemereignisse abonnieren:

-   Einrichtung der Netzwerkkonnektivität
-   Benachrichtigung, wenn ein angegebenes Ziel innerhalb der angegebenen QOC-Parameter (Quality of Connection) erreicht werden kann
-   Der Computer wurde in den Akkubetrieb umgeschaltet.
-   Der Prozentsatz der verbleibenden Akkuleistung liegt innerhalb eines angegebenen Parameters.
-   Geplante Ereignisse mit dem Synchronisierungs-Manager treten auf

**Windows Server 2008 R2 und Windows 7:** Der Abonnent hat maximal drei Minuten Zeit, um auf eine Benachrichtigung über die Schnittstellen [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) und [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) zu reagieren. Nach 3 Minuten bricht SENS den Aufruf von Abonnenten ab und hebt die Blockierung des Benachrichtigungsthreads auf. Wenn ein längerer Vorgang erforderlich ist, um auf die Benachrichtigung zu reagieren, kehren Sie so schnell wie möglich von **ISensLogon** oder **ISensLogon2** zurück, und öffnen Sie einen anderen Thread für die Verarbeitung.

 

 



