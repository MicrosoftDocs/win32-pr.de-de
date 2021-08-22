---
title: Informationen zu Traps und Benachrichtigungen
description: Eine Art von Nachricht, die eine SNMP-Agentanwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein signifikantes Ereignis informiert.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009808"
---
# <a name="about-traps-and-notifications"></a>Informationen zu Traps und Benachrichtigungen

Eine Art von Nachricht, die eine SNMP-Agentanwendung an eine WinSNMP-Anwendung senden kann, ist eine asynchrone Nachricht, die die Anwendung über ein signifikantes Ereignis informiert. Ein Beispiel für ein signifikantes Ereignis ist das Herunterfahren einer Netzwerkverbindung oder das Auftreten eines Authentifizierungsfehlers.

Diese Nachrichtentypen werden unter SNMPv1 als Traps und unter SNMPv2C als Benachrichtigungen bezeichnet. Die Microsoft WinSNMP-Implementierung übersetzt SNMPv1-Traps immer in das SNMPv2C-Format, wie in RFC 1908 definiert.

Wenn Sie die [**SnmpCreatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, um ein Trap-PDU zu erstellen, können Sie nur ein SNMPv2C-Trap-PDU erstellen. Der einzige Typ von Trap-PDU, den Sie mit einem Aufruf der [**SnmpSetPduData-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) aktualisieren können, ist ein SNMPv2C-Trap-PDU.

Weitere Informationen finden Sie in den folgenden Themen.



| Thema                                                                                    | Beschreibung |
|------------------------------------------------------------------------------------------|-------------|
| [Übersetzen von Traps von SNMPv1 in SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Trapformate](trap-formats.md)                                                         |             |



 

 

 




