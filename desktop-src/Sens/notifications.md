---
description: Mithilfe des System Ereignis Benachrichtigungs Diensts können Anwendungen, die von der System Ereignis Benachrichtigung überwachen, Benachrichtigungen von System Ereignissen empfangen. Wenn das angeforderte Ereignis auftritt, benachrichtigt Sens die Anwendung.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Benachrichtigungen (System Ereignis Benachrichtigungsdienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359464"
---
# <a name="notifications-system-event-notification-service"></a>Benachrichtigungen (System Ereignis Benachrichtigungsdienst)

Mithilfe des System Ereignis Benachrichtigungs Diensts können Anwendungen, die von der System Ereignis Benachrichtigung überwachen, Benachrichtigungen von System Ereignissen empfangen. Wenn das angeforderte Ereignis auftritt, benachrichtigt Sens die Anwendung.

Sens kann Anwendungen über drei Klassen von System Ereignissen Benachrichtigen:

-   TCP/IP-Netzwerkereignisse, z. b. der Status einer TCP/IP-Netzwerkverbindung oder die Qualität der Verbindung.
-   Benutzer Anmelde Ereignisse.
-   Akku-und Strom Leistungs Ereignisse.

Beispielsweise kann eine Anwendung eines der folgenden Systemereignisse abonnieren:

-   Einrichtung der Netzwerk Konnektivität
-   Benachrichtigung, wenn ein angegebenes Ziel innerhalb der angegebenen qoc (Quality of Connection)-Parameter erreicht werden kann
-   Der Computer wurde in den Akku Betrieb gewechselt.
-   Der Prozentsatz der verbleibenden Akkuleistung liegt innerhalb eines angegebenen Parameters.
-   Geplante Ereignisse mithilfe des Synchronisierungs-Managers

**Windows Server 2008 R2 und Windows 7:** Der Abonnent hat maximal 3 Minuten Zeit, um auf eine Benachrichtigung über die [**isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) -und [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) -Schnittstellen zu antworten. Nach drei Minuten bricht er den Rückruf von Abonnenten ab und hebt die Blockierung des Benachrichtigungs Threads auf. Wenn ein längerer Vorgang erforderlich ist, um auf die Benachrichtigung zu antworten, kehren Sie von **isenslogon** oder **ISensLogon2** so schnell wie möglich zurück, und öffnen Sie einen anderen Thread für die Verarbeitung.

 

 



