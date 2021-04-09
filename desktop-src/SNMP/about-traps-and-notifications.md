---
title: Informationen zu Traps und Benachrichtigungen
description: Eine Nachricht, die eine SNMP-Agent-Anwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein wichtiges Ereignis informiert.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856192"
---
# <a name="about-traps-and-notifications"></a>Informationen zu Traps und Benachrichtigungen

Eine Nachricht, die eine SNMP-Agent-Anwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein wichtiges Ereignis informiert. Ein Beispiel für ein wichtiges Ereignis ist, wenn eine Netzwerkverbindung heruntergefahren wird oder wenn ein Authentifizierungsfehler auftritt.

Diese Nachrichten Typen werden unter SNMPv1 und Benachrichtigungen unter SNMPv2C als Traps bezeichnet. Die Microsoft WinSNMP-Implementierung übersetzt SNMPv1 Traps immer in das SNMPv2C-Format, wie in RFC 1908 definiert.

Wenn Sie die Funktion [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, um ein Trap-PDU zu erstellen, können Sie nur ein SNMPv2C Trap-PDU erstellen. Der einzige Typ von Trap-PDU, den Sie mit einem Aufrufen der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aktualisieren können, ist ein SNMPv2C Trap-PDU.

Weitere Informationen finden Sie in den nachfolgenden Themen.



| Thema                                                                                    | BESCHREIBUNG |
|------------------------------------------------------------------------------------------|-------------|
| [Übersetzen von Traps von SNMPv1 in SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Trap-Formate](trap-formats.md)                                                         |             |



 

 

 




