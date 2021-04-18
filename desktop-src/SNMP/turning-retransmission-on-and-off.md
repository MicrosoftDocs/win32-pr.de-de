---
title: Aktivieren und Deaktivieren der erneuten Übertragung
description: Eine Anwendung kann den Modus für Neuübertragungen mit einem aufzurufenden Befehl der snmpsetretransmitmode-Funktion festlegen. Der neue Neuübertragungs Modus gilt für nachfolgende Aufrufe der snmpsendmsg-Funktion.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340418"
---
# <a name="turning-retransmission-on-and-off"></a>Aktivieren und Deaktivieren der erneuten Übertragung

Eine Anwendung kann den Modus für Neuübertragungen mit einem aufzurufenden Befehl der [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion festlegen. Der neue Neuübertragungs Modus gilt für nachfolgende Aufrufe der [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion.

Wenn die Anwendung **snmpsetretransmitmode** mit dem Neuübertragungs-Moduswert Snmpapi \_ on aufruft, beginnt die Microsoft WinSNMP-Implementierung mit der Ausführung der Neuübertragungs Richtlinie der Anwendung. Der neue Modus für Neuübertragungen wirkt sich nicht auf ausstehende SNMP-Nachrichten aus. Eine ausstehende Meldung ist eine Meldung, die zu dem Zeitpunkt, zu dem die Anwendung den Modus für die Neuübertragung ändert, keine Antwort hat.

Wenn die WinSNMP-Anwendung die [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion mit dem Neuübertragungs-Moduswert Snmpapi \_ Off aufruft, beendet die-Implementierung die Ausführung der Richtlinie zum erneuten übertragen. Die-Implementierung bricht Neuübertragungs Versuche für ausstehende SNMP-Nachrichten ab. Dies liegt daran, dass es möglicherweise nicht möglich ist, dass die Implementierung alle ausstehenden SNMP-Anforderungen und-Vorgänge zuzüglich neuer Anforderungen verarbeitet, bevor ein Anwendungs Timeout oder ein Wiederholungsversuch ein Ereignis signalisiert.

 

 




