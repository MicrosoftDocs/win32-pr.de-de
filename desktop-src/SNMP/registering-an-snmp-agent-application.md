---
title: Registrieren einer SNMP-Agent-Anwendung
description: Neben SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2.0 auch SNMP-Agent-Vorgänge.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009128"
---
# <a name="registering-an-snmp-agent-application"></a>Registrieren einer SNMP-Agent-Anwendung

Neben SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2.0 auch SNMP-Agent-Vorgänge.

Um eine WinSNMP-Anwendung als SNMP-Agent zu registrieren, kann die Anwendung die [**SnmpListen-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) aufrufen. Diese Funktion informiert die Microsoft WinSNMP-Implementierung darüber, dass eine SNMP-Entität in der Rolle eines SNMP-Agents agiert. Die Anwendung kann auch **SnmpListen** aufrufen, um die Implementierung zu informieren, wenn sie nicht mehr als Agent fungiert.

Wenn eine Anwendung die [**SnmpListen-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) aufruft und den Wert SNMPAPI \_ ON im *lStatus-Parameter* übergibt, werden die folgenden Aktionen ausgeführt:

1.  Die Entität, die in einer SNMP-Agentrolle funktioniert, wird an ihren zugewiesenen Port gebunden und lauscht auf eingehende SNMP-Nachrichtenanforderungen.
2.  Der Agent verwendet anwendungsspezifische Logik, um jede SNMP-Anforderung zu verarbeiten.
3.  Der Agent bildet geeignete Antworten auf jede Anforderung.
4.  Der Agent überträgt die Antwort an die anfordernde Entität, indem er die [**SnmpSendMsg-Funktion aufruft.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) Wenn der Agent **SnmpSendMsg** aufruft, gibt er die Adresse des Agents im *srcEntity-Parameter* und die Adresse der Remote-Manager-Entität im *dstEntity-Parameter* an. (Diese Werte sind die Umkehrung der Werte, die die Agententität in diesen Parametern empfangen hat, als sie die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) aufgerufen hat, um eine SNMP-Anforderung abzurufen.)

Weitere Informationen zu SNMP-Verwaltungsanwendungen und Agent-Anwendungen finden Sie unter [Informationen zu SNMP.](about-snmp.md)

 

 




