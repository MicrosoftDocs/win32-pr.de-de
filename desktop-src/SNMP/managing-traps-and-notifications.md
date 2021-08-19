---
title: Verwalten von Traps und Benachrichtigungen
description: Die WinSNMP-Anwendung muss sich registrieren, um Traps und Benachrichtigungen zu empfangen, indem sie die SnmpRegister-Funktion mit SNMPAPI \_ ON aufruft. Die Anwendung kann die Registrierung aufheben und Traps und Benachrichtigungen deaktivieren, indem sie die Funktion mit SNMPAPI \_ OFF aufruft.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009378"
---
# <a name="managing-traps-and-notifications"></a>Verwalten von Traps und Benachrichtigungen

Die WinSNMP-Anwendung muss sich registrieren, um Traps und Benachrichtigungen zu empfangen, indem sie die [**SnmpRegister-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) mit SNMPAPI \_ ON aufruft. Die Anwendung kann die Registrierung aufheben und Traps und Benachrichtigungen deaktivieren, indem sie die Funktion mit SNMPAPI \_ OFF aufruft.

Wenn die Anwendung **SnmpRegister** aufruft, stehen mehrere Optionen zur Verfügung. Die Anwendung kann die Registrierung für die folgenden Traps und Benachrichtigungen aufheben:

-   Eine Art von Trap oder Benachrichtigung
-   Alle Traps und Benachrichtigungen
-   Alle Quellen von Trap- und Benachrichtigungsanforderungen
-   Traps und Benachrichtigungen von allen Verwaltungsentitäten
-   Traps und Benachrichtigungen für jeden Kontext

Um einen vordefinierten Trap- oder Benachrichtigungstyp zu registrieren und zu empfangen, muss die Anwendung einen Objektbezeichner (eine [**smiOID-Struktur)**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) für jeden vordefinierten Typ definieren. Die -Struktur muss eine Musterabgleichssequenz für den Typ des Traps oder der Benachrichtigung enthalten. RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)" definiert Trap- und Benachrichtigungsobjektbezeichner.

Um ausstehende Trapdaten und Benachrichtigungen für eine WinSNMP-Sitzung abzurufen, muss eine WinSNMP-Anwendung die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) mit dem von der [**SnmpCreateSession-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) zurückgegebenen Sitzungshandle aufrufen.

Weitere Informationen finden Sie unter [Senden von SNMP-Nachrichten](sending-snmp-messages.md) und [Empfangen von SNMP-Nachrichten.](receiving-snmp-messages.md) Weitere Informationen zur Zuordnung und Freigabe von Ressourcen für Traps und Benachrichtigungen finden Sie unter [Zuordnen von WinSNMP-Speicherobjekten.](allocating-winsnmp-memory-objects.md)

 

 




