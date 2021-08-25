---
title: Aktivieren und Deaktivieren der Neuübertragung
description: Eine Anwendung kann den Neuübertragungsmodus mit einem Aufruf der SnmpSetRetransmitMode-Funktion festlegen. Der neue Neuübertragungsmodus gilt für nachfolgende Aufrufe der SnmpSendMsg-Funktion.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7624977b4959911cc4128c9a75ac70fac7031bfb853c4b31db34d0987b4d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885670"
---
# <a name="turning-retransmission-on-and-off"></a>Aktivieren und Deaktivieren der Neuübertragung

Eine Anwendung kann den Neuübertragungsmodus mit einem Aufruf der [**SnmpSetRetransmitMode-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) festlegen. Der neue Neuübertragungsmodus gilt für nachfolgende Aufrufe der [**SnmpSendMsg-Funktion.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

Wenn die Anwendung **SnmpSetRetransmitMode** mit dem Wert für den Neuübertragungsmodus SNMPAPI \_ ON aufruft, beginnt die Microsoft WinSNMP-Implementierung mit der Ausführung der Neuübertragungsrichtlinie der Anwendung. Der neue Neuübertragungsmodus wirkt sich nicht auf ausstehende SNMP-Nachrichten aus. Eine ausstehende Nachricht ist eine Nachricht, die zu dem Zeitpunkt, zu dem die Anwendung den Neuübertragungsmodus ändert, keine Antwort hat.

Wenn die WinSNMP-Anwendung die [**SnmpSetRetransmitMode-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) mit dem Wert für den Neuübertragungsmodus SNMPAPI \_ OFF aufruft, beendet die Implementierung die Ausführung der Neuübertragungsrichtlinie. Die Implementierung bricht Neuübertragungsversuche für ausstehende SNMP-Nachrichten ab. Dies liegt daran, dass es für die Implementierung möglicherweise nicht möglich ist, alle ausstehenden SNMP-Anforderungen und -Vorgänge sowie neue Anforderungen zu verarbeiten, bevor ein Time-Out oder ein Wiederholungsindikator der Anwendung ein Ereignis signalisiert.

 

 




