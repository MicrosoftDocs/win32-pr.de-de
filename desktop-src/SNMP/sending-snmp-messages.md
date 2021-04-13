---
title: Senden von SNMP-Nachrichten
description: Eine WinSNMP-Anwendung initiiert eine Übertragungs Anforderung durch Senden einer SNMP-Nachricht. SNMP-Nachrichten enthalten eine SNMP-Protokolldaten Einheit. Weitere Informationen finden Sie unter Arbeiten mit Protokolldaten Einheiten.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310715"
---
# <a name="sending-snmp-messages"></a>Senden von SNMP-Nachrichten

Eine WinSNMP-Anwendung initiiert eine Übertragungs Anforderung durch Senden einer SNMP-Nachricht. SNMP-Nachrichten enthalten eine SNMP-Protokolldaten Einheit. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).

Eine WinSNMP-Anwendung muss die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) anrufen, um anzufordern, dass die Microsoft WinSNMP-Implementierung das PDU mit den anderen erforderlichen Nachrichten Elementen überträgt, die von der entsprechenden RFC definiert werden. Neben der Ziel Entität muss die Anwendung die Quell Entität und einen Kontext für die Anforderung angeben. Die [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion wird asynchron ausgeführt.

Die Anwendung WinSNMP muss die Funktion [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufrufen, um die Antwort auf eine **snmpsendmsg** -Anforderung abzurufen.

Die-Implementierung überprüft die Gültigkeit des PDU-und der anderen Message-Elemente, wenn eine Anwendung [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)aufruft.

 

 




