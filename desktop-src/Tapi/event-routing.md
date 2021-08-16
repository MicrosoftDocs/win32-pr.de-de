---
description: Mit der lineSetTerminal-Funktion kann die Anwendung das Routing von angegebenen Ereignissen auf niedriger Ebene (die zwischen dem Switch und der Station ausgetauscht werden) an ein Gerät steuern oder unterdrücken.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Ereignisrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c71d07994090a1e68fcbadd1cd3b686a3de316e4a6fd01cca506fcdbcdbd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763095"
---
# <a name="event-routing"></a>Ereignisrouting

Mit der [**lineSetTerminal-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) kann die Anwendung das Routing von angegebenen Ereignissen auf niedriger Ebene (die zwischen dem Switch und der Station ausgetauscht werden) an ein Gerät steuern oder unterdrücken. Mit **lineSetTerminal** gibt die Anwendung das Terminalgerät an, an das diese Ereignisse (z. B. Zeilen-, Adress- oder Aufrufmedienstreamereignisse) weitergeleitet werden.

Das Routing der verschiedenen Ereignisklassen kann einzeln gesteuert werden, sodass für jede Ereignisklasse separate Terminals angegeben werden können. Zu den Ereignisklassen gehören Unterführung, Schaltflächen, Anzeige, Ringer, Hookswitch und Medienstream.

Beispielsweise kann der Mediendatenstrom eines Anrufs (z. B. Sprache) an jedes Transducergerät gesendet werden, wenn der Dienstanbieter und die Hardware dazu in der Lage sind. Im Allgemeinen bedeutet ein *Transducer* dasselbe wie ein *hookswitch-Gerät* in TAPI, das über ein Mikrofon und einen Lautsprecher verfügt. Ringereignisse vom Switch zum Telefon können einer visuellen Warnung auf dem Bildschirm des Computers zugeordnet oder an ein Telefongerät weitergeleitet werden. Lamp-Ereignisse und Anzeigeereignisse können ignoriert oder an ein Telefongerät weitergeleitet werden (das sich scheinbar wie ein normaler Telefonsatz verhält). Schließlich können Tastendrucke auf einem Telefongerät an die Zeile übergeben werden. In jedem Fall wirkt sich dieses Routing von Signalen auf niedriger Ebene von der Linie nicht auf den Betrieb des Linienteils von TAPI aus, der ereignisse auf niedriger Ebene immer ihrer funktionalen Entsprechung zuteilt. Um die Terminals zu ermitteln, die ein Liniengerät zur Verfügung hat (und deren Funktionen), lesen Sie die Funktionen des Liniengeräts mit [**lineGetDevCaps.**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)

Angenommen, die Anwendung hat zunächst das Routing aller Ereignisse unterdrückt (mit [**lineSetTerminal),**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)und der Benutzer wählt ein Headset als aktuelles E/A-Gerät aus. Ein eingehender Aufruf sendet eine [**LINE \_ CALLSTATE-Nachricht**](line-callstate.md) und eine [**LINE \_ LINEDEVSTATE-Nachricht**](line-linedevstate.md) mit der *Ringanzeige.* Da das Routing aller Ereignisse unterdrückt wird, werden Ringereignisse nicht an das Telefon weitergeleitet, sodass das Ringen unterdrückt wird. Stattdessen benachrichtigt die Anwendung den Benutzer mit einem Popupdialogfeld und einem Systemsignal im Headset.

Der Benutzer entscheidet sich, den Anruf zu beantworten. Da das aktuelle E/A-Gerät des Benutzers das Headset ist, ruft die Telefonieanwendung [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) beim eingehenden Anruf auf, um die Medien des Anrufs an das Headset weiterzuleiten und den Anruf zu beantworten. Die Anwendung kann auch **lineSetTerminal** aufrufen, um Lampe weiterzuleiten und Informationsereignisse an den Telefonsatz anzuzeigen, sodass sie sich wie gewohnt verhält.

Als zweites Beispiel wird davon ausgegangen, dass ein eingehender Anruf eine Warnung auf dem Computer des Benutzers auslöst. Anstatt die Antwortoption mit der Maus auszuwählen, entscheidet sich der Benutzer, einfach das Mobiltelefon abzuholen, um den Anruf zu beantworten. Der Offhookstatus am Telefon sendet eine Nachricht an die Anwendung. Die Anwendung kann diesen Status als Anforderung des Benutzers interpretieren, das Mobiltelefon auszuwählen, um die Konversation durchzuführen. Die Anwendung ruft dann [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) auf, um die Sprachdaten beim Anruf an den Telefonsatz weiterzuleiten.

 

 



