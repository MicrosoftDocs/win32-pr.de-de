---
description: Mit der linesetterminal-Funktion kann die Anwendung das Routing von angegebenen Ereignissen auf niedriger Ebene (zwischen dem Switch und der Station ausgetauscht) an ein Gerät steuern oder unterdrücken.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Ereignisrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360047"
---
# <a name="event-routing"></a>Ereignisrouting

Mit der [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) -Funktion kann die Anwendung das Routing von angegebenen Ereignissen auf niedriger Ebene (zwischen dem Switch und der Station ausgetauscht) an ein Gerät steuern oder unterdrücken. Mit **linesetterminal** gibt die Anwendung das Terminal Gerät an, auf das diese Ereignisse (z. b. Line-, address-oder callmedia-Stream-Ereignisse) weitergeleitet werden.

Das Routing der verschiedenen Klassen von Ereignissen kann einzeln gesteuert werden, sodass für jede Ereignisklasse separate Terminals angegeben werden können. Zu den Ereignis Klassen zählen Lampen, Schaltflächen, Anzeige, stumm, anokswitch und Mediendaten Strom.

So kann z. b. der Mediendaten Strom eines-Aufrufes (z. b. Voice) an ein beliebiges Übertragungs Gerät gesendet werden, wenn der Dienstanbieter und die Hardware dies tun können. Im Allgemeinen bedeutet ein " *Transducer* " dasselbe wie ein " *huokswitch* "-Gerät in TAPI, etwas, das über ein Mikrofon und einen Redner verfügt. Ring Ereignisse von der Umstellung auf das Telefon können einer visuellen Warnung auf dem Computerbildschirm zugeordnet werden, oder Sie können zu einem Telefongerät weitergeleitet werden. Lamp-Ereignisse und Anzeige Ereignisse können ignoriert oder an ein Telefongerät weitergeleitet werden (was sich als normales Telefon Satz verhält). Zum Schluss kann es sein, dass Schaltflächen auf einem Telefongerät an die Zeile geleitet werden. In jedem Fall wirkt sich dieses Routing von Signalen auf niedriger Ebene von der Zeile nicht auf den Betrieb des Linien Teils von TAPI aus, der immer auf Low-Level-Ereignissen ihrer funktionalen Entsprechung zuordnet. Um zu ermitteln, welche Terminals ein liniengerät (und seine Funktionen) verfügbar ist, überprüfen Sie die Funktionen des Geräts mit [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Angenommen, die Anwendung hat das Routing aller Ereignisse (mit [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)) unterdrückt, und der Benutzer wählt ein Headset als Aktuelles e/a-Gerät aus. Ein eingehender Aufruf sendet eine [**zeilige \_ CallState**](line-callstate.md) -Nachricht und [**eine \_ linedevstate-linienmeldung**](line-linedevstate.md) mit der *Klingel* Angabe. Da das Routing aller Ereignisse unterdrückt wird, werden Ring Ereignisse nicht an das Telefon weitergeleitet, sodass das Klingeln unterdrückt wird. Stattdessen wird der Benutzer von der Anwendung ein Popup Dialogfeld und ein Systemsignal im Headset benachrichtigt.

Der Benutzer beschließt, den Anruf zu beantworten. Da es sich bei dem aktuellen e/a-Gerät des Benutzers um das Headset handelt, ruft die Telefonieanwendung [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) bei dem eingehenden Aufruf auf, um die Medien des aufgerufenen an das Headset weiterzuleiten und den Anruf zu beantworten Die Anwendung kann auch **linesetterminal** aufrufen, um Lamp zu leiten und Informations Ereignisse an den Telefon Satz anzuweisen, sodass Sie sich wie gewohnt verhält.

Nehmen Sie als zweites Beispiel an, dass ein eingehender-Rückruf auf dem Computer des Benutzers eine Warnung durchläuft. Anstatt mit der Maus auf die Option "Antwort" zu klicken, entscheidet sich der Benutzer dazu, einfach das Handy des Telefons auszuwählen, um den Anruf zu beantworten. Der OFFHOOK-Status auf dem Telefon sendet eine Meldung an die Anwendung. Die Anwendung kann diesen Status als Anforderung vom Benutzer interpretieren, um das Telefongerät zum Durchführen der Konversation auszuwählen. Die Anwendung ruft dann [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) auf, um die Sprach Daten beim Aufruf an den Telefon Satz weiterzuleiten.

 

 



