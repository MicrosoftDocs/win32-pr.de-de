---
title: Verwalten von Traps und Benachrichtigungen
description: Die WinSNMP-Anwendung muss registriert werden, um Traps und Benachrichtigungen zu empfangen, indem die SnmpRegister-Funktion mit Snmpapi auf aufgerufen wird \_ . Die Anwendung kann die Registrierung und die Deaktivierung von Traps und Benachrichtigungen aufheben, indem Sie die-Funktion mit Snmpapi \_ Off aufrufen.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856632"
---
# <a name="managing-traps-and-notifications"></a>Verwalten von Traps und Benachrichtigungen

Die WinSNMP-Anwendung muss registriert werden, um Traps und Benachrichtigungen zu empfangen, indem die [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) -Funktion mit Snmpapi auf aufgerufen wird \_ . Die Anwendung kann die Registrierung und die Deaktivierung von Traps und Benachrichtigungen aufheben, indem Sie die-Funktion mit Snmpapi \_ Off aufrufen.

Wenn die Anwendung **snmpregiester** aufruft, stehen mehrere Optionen zur Verfügung. Die Anwendung kann sich für die folgenden Traps und Benachrichtigungen registrieren oder die Registrierung aufheben:

-   Ein Typ von Trap oder Benachrichtigung
-   Alle Traps und Benachrichtigungen
-   Alle Quellen von Trap-und Benachrichtigungs Anforderungen
-   Traps und Benachrichtigungen von allen Verwaltungs Entitäten
-   Traps und Benachrichtigungen für jeden Kontext

Zum Registrieren und Empfangen eines vordefinierten Traps oder Benachrichtigungs Typs muss die Anwendung für jeden vordefinierten Typ einen Objekt Bezeichner (eine [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur) definieren. Die-Struktur muss eine Muster Vergleichs Sequenz für den Typ von Trap oder Benachrichtigung enthalten. RFC 1907, "Verwaltungs Informationsbasis für Version 2 des Simple Network Management-Protokolls (SNMPv2)", definiert Trap-und Benachrichtigungs Objekt-IDs.

Zum Abrufen von ausstehenden Trap Daten und Benachrichtigungen für eine WinSNMP-Sitzung muss eine WinSNMP-Anwendung die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion mit dem Sitzungs handle aufrufen, das von der [**snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) -Funktion zurückgegeben wird.

Weitere Informationen finden Sie unter [Senden von SNMP-Nachrichten](sending-snmp-messages.md) und [empfangen von SNMP-Nachrichten](receiving-snmp-messages.md). Weitere Informationen zur Zuordnung und Aufhebung der Zuordnung von Ressourcen für Traps und Benachrichtigungen finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).

 

 




