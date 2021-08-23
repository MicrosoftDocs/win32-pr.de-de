---
title: WinSNMP-API
description: Mit den Versionen 1.1a und 2.0 der Microsoft Windows SNMP Application Programming Interface (WinSNMP-API) können Sie SNMP-basierte Netzwerkverwaltungsanwendungen entwickeln, die in der Windows Umgebung ausgeführt werden.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- WinSNMP-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38f6205b8d5ad2315be877f62f0f81f17b5737e557d5db2683163ff26edf62c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142983"
---
# <a name="winsnmp-api"></a>WinSNMP-API

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Mit den Versionen 1.1a und 2.0 der Microsoft Windows SNMP Application Programming Interface (WinSNMP-API) können Sie SNMP-basierte Netzwerkverwaltungsanwendungen entwickeln, die in der Windows Umgebung ausgeführt werden. Das Simple Network Management Protocol (SNMP) ist ein Anforderung-Antwort-Protokoll, das Verwaltungsinformationen zwischen Protokollentitäten überträgt.

WinSNMP wurde gemeinsam mit der Zusammenarbeit, Eingabe und Unterstützung mehrerer Unternehmen, Organisationen und Einzelpersonen entwickelt.

Der erste Teil dieser Übersicht enthält Informationen zum WinSNMP 2.0-Nachtrag, zu den SNMP-Versionen und eine Liste der relevanten Requests for Comments (RFCs). Außerdem werden das WinSNMP-Modell und die Komponenten und Features der Microsoft WinSNMP-Implementierung beschrieben. Außerdem enthält sie Informationen zu Datenverwaltungs- und Kommunikationskonzepten, die Sie in der WinSNMP-Umgebung programmieren müssen.

Im zweiten Abschnitt werden die WinSNMP-Funktionen und die folgenden zugehörigen WinSNMP-Programmieraufgaben erläutert:

-   [Öffnen und Schließen einer WinSNMP-Anwendung](opening-and-closing-a-winsnmp-application.md)
-   [Öffnen und Schließen einer WinSNMP-Sitzung](opening-and-closing-a-winsnmp-session.md)
-   [Verwalten von Traps und Benachrichtigungen](managing-traps-and-notifications.md)
-   [Arbeiten mit Variablenbindungslisten](working-with-variable-binding-lists.md)
-   [Arbeiten mit Protokolldateneinheiten](working-with-protocol-data-units.md)
-   [Senden von SNMP-Nachrichten](sending-snmp-messages.md)
-   [Empfangen von SNMP-Nachrichten](receiving-snmp-messages.md)
-   [Verwalten von Objektbezeichnern](managing-object-identifiers.md)
-   [Freigeben von WinSNMP-Deskriptoren](freeing-winsnmp-descriptors.md)
-   [Festlegen des Entitäts- und Kontextübersetzungsmodus](setting-the-entity-and-context-translation-mode.md)
-   [Verwalten der Neuübertragungsrichtlinie](managing-the-retransmission-policy.md)
-   [Schreiben von WinSNMP-Anwendungen mit mehreren Threads](writing-winsnmp-applications-with-multiple-threads.md)
-   [Registrieren einer SNMP-Agent-Anwendung](registering-an-snmp-agent-application.md)

Sie sollten mit den grundlegenden Konzepten von SNMP und Windows Programmierung vertraut sein, bevor Sie diese Übersicht lesen. Weitere Informationen zu SNMP finden Sie unter [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) und die relevanten RfCs (Requests for Comments), die von der Internet Engineering Task Force (IETF) veröffentlicht werden.

 

 