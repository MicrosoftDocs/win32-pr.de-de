---
title: Registrieren einer SNMP-Agent-Anwendung
description: Zusätzlich zu den SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2,0 auch SNMP-Agent-Vorgänge.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947891"
---
# <a name="registering-an-snmp-agent-application"></a>Registrieren einer SNMP-Agent-Anwendung

Zusätzlich zu den SNMP-Manager-Vorgängen unterstützt die WinSNMP-API-Version 2,0 auch SNMP-Agent-Vorgänge.

Um eine WinSNMP-Anwendung als SNMP-Agent zu registrieren, kann die Anwendung die [**snmpl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) abrufen. Diese Funktion informiert die Microsoft WinSNMP-Implementierung, dass eine SNMP-Entität in der Rolle eines SNMP-Agents fungiert. Die Anwendung kann auch **snmplauschen** aufzurufen, um die Implementierung zu informieren, wenn Sie nicht mehr als Agent fungiert.

Wenn eine Anwendung die [**snmpabhör**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) -Funktion aufruft und den Wert "Snmpapi" \_ im *lstatus* -Parameter übergibt, treten die folgenden Aktionen auf:

1.  Die Entität, die in einer SNMP-agentrolle funktioniert, bindet Sie an ihren zugewiesenen Port und lauscht auf eingehende SNMP-Nachrichten Anforderungen.
2.  Der Agent verwendet anwendungsspezifische Logik, um jede SNMP-Anforderung zu verarbeiten.
3.  Der Agent bildet geeignete Antworten auf die einzelnen Anforderungen.
4.  Der Agent überträgt die Antwort an die anfordernde Entität, indem er die [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion aufrufen. Wenn der Agent **snmpsendmsg** aufruft, gibt er die Adresse des Agents im *srcentity* -Parameter und die Adresse der Remote-Manager-Entität im *dstentity* -Parameter an. (Diese Werte sind das Gegenteil der Werte, die die agententität in diesen Parametern erhalten hat, als die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion zum Abrufen einer SNMP-Anforderung aufgerufen wurde.)

Weitere Informationen zu SNMP-Verwaltungs Anwendungen und-Agent-Anwendungen finden Sie unter [Informationen zu SNMP](about-snmp.md).

 

 




