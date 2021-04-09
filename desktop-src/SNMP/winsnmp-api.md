---
title: WinSNMP-API
description: Mit der Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (der WinSNMP-API) Version 1.1 a und 2,0 können Sie SNMP-basierte Netzwerk Verwaltungs Anwendungen entwickeln, die in der Windows-Umgebung ausgeführt werden.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039325"
---
# <a name="winsnmp-api"></a>WinSNMP-API

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Mit der Microsoft Windows SNMP-Anwendungsprogrammierschnittstelle (der WinSNMP-API) Version 1.1 a und 2,0 können Sie SNMP-basierte Netzwerk Verwaltungs Anwendungen entwickeln, die in der Windows-Umgebung ausgeführt werden. Das Simple Network Management-Protokoll (SNMP) ist ein Anforderungs Antwort Protokoll, das Verwaltungsinformationen zwischen Protokoll Entitäten überträgt.

WinSNMP wurde gemeinsam mit der Zusammenarbeit, der Eingabe und der Unterstützung von mehreren Unternehmen, Zuordnungen und Einzelpersonen entwickelt.

Der erste Teil dieser Übersicht enthält Informationen über den WinSNMP 2,0-Nachtrag, SNMP-Versionen und eine Liste der relevanten Anfragen für Kommentare (RFCs). Außerdem werden das WinSNMP-Modell und die Komponenten und Funktionen der Microsoft WinSNMP-Implementierung beschrieben. Außerdem finden Sie hier Informationen zu Daten Verwaltungs-und Kommunikationskonzepten, die Sie in der WinSNMP-Umgebung programmieren müssen.

Im zweiten Abschnitt werden die WinSNMP-Funktionen und die folgenden verwandten WinSNMP-Programmieraufgaben erläutert:

-   [Öffnen und Schließen einer WinSNMP-Anwendung](opening-and-closing-a-winsnmp-application.md)
-   [Öffnen und Schließen einer WinSNMP-Sitzung](opening-and-closing-a-winsnmp-session.md)
-   [Verwalten von Traps und Benachrichtigungen](managing-traps-and-notifications.md)
-   [Arbeiten mit Variablen Bindungs Listen](working-with-variable-binding-lists.md)
-   [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md)
-   [Senden von SNMP-Nachrichten](sending-snmp-messages.md)
-   [Empfangen von SNMP-Nachrichten](receiving-snmp-messages.md)
-   [Verwalten von Objekt bezeichlern](managing-object-identifiers.md)
-   [Freigeben von WinSNMP-Deskriptoren](freeing-winsnmp-descriptors.md)
-   [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md)
-   [Verwalten der Richtlinie für Neuübertragungen](managing-the-retransmission-policy.md)
-   [Schreiben von WinSNMP-Anwendungen mit mehreren Threads](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrieren einer SNMP-Agent-Anwendung](registering-an-snmp-agent-application.md)

Bevor Sie diese Übersicht lesen, sollten Sie mit den grundlegenden Konzepten der SNMP-und Windows-Programmierung vertraut sein. Weitere Informationen zu SNMP finden Sie unter [Simple Network Management Protocol (Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) ) und in den von der Internet Engineering Task Force (IETF) veröffentlichten Anforderungen für Kommentare (RFCs).

 

 