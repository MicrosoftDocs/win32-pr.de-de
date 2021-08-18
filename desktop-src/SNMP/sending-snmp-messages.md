---
title: Senden von SNMP-Nachrichten
description: Eine WinSNMP-Anwendung initiiert eine Übertragungsanforderung, indem eine SNMP-Nachricht gesendet wird. SNMP-Nachrichten enthalten eine SNMP-Protokolldateneinheit. Weitere Informationen finden Sie unter Arbeiten mit Protokolldateneinheiten.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009068"
---
# <a name="sending-snmp-messages"></a>Senden von SNMP-Nachrichten

Eine WinSNMP-Anwendung initiiert eine Übertragungsanforderung, indem eine SNMP-Nachricht gesendet wird. SNMP-Nachrichten enthalten eine SNMP-Protokolldateneinheit. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldateneinheiten.](working-with-protocol-data-units.md)

Eine WinSNMP-Anwendung muss die [**SnmpSendMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) aufrufen, um anzufordern, dass die Microsoft WinSNMP-Implementierung die PDU mit den anderen erforderlichen Nachrichtenelementen überträgt, die von der relevanten RFC definiert werden. Zusätzlich zur Zielentität muss die Anwendung die Quellentität und einen Kontext für die Anforderung angeben. Die [**SnmpSendMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) wird asynchron ausgeführt.

Die WinSNMP-Anwendung muss die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufrufen, um die Antwort auf eine **SnmpSendMsg-Anforderung** abzurufen.

Die Implementierung überprüft die Gültigkeit der PDU und der anderen Nachrichtenelemente, wenn eine Anwendung [**SnmpSendMsg aufruft.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

 

 




