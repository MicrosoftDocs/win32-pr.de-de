---
title: Empfangen von SNMP-Nachrichten
description: Die WinSNMP-Anwendung muss die SnmpRecvMsg-Funktion aufrufen, um die Antwort auf eine SnmpSendMsg-Anforderung abzurufen.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009178"
---
# <a name="receiving-snmp-messages"></a>Empfangen von SNMP-Nachrichten

Die WinSNMP-Anwendung muss die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufrufen, um die Antwort auf eine [**SnmpSendMsg-Anforderung abzurufen.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

Die [**SnmpCreateSession-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) übergibt ein Anwendungsfensterhandl und eine Benachrichtigungsmeldungs-ID an die Microsoft WinSNMP-Implementierung. Wenn das Anwendungsfenster diese Meldung empfängt, signalisiert es der Anwendung, die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) mithilfe des sitzungshandlers aufzugeben, das von [**SnmpCreateSession zurückgegeben wird.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)

Die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) gibt zwei Entitätshandles, ein Kontexthandles und das Handle an ein PDU zurück. Es wird empfohlen, dass die WinSNMP-Anwendung diese Ressourcen mithilfe der [**Funktionen SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)und [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) frei gibt.

Weitere Informationen zum Verwalten der Zeit zwischen einem Aufruf der [**SnmpSendMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) und dem Empfang der entsprechenden Antwort finden Sie unter Informationen zur [Neuübertragung](about-retransmission.md)von . Weitere Informationen zur Verwendung des PDU-Felds der Anforderungs-ID zum Abgleichen eines Antwort-PDU mit dem Anforderungs-PDU finden Sie unter Abgleichen von [Antwort- und Anforderungs-PDUs.](matching-response-and-request-pdus.md) **\_**

 

 




