---
title: Informationen zu SNMP
description: SNMP verwendet eine verteilte Architektur, bestehend aus Managern und Agents.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039434"
---
# <a name="about-snmp"></a>Informationen zu SNMP

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

SNMP verwendet eine verteilte Architektur, bestehend aus Managern und Agents. Ein Agent ist eine SNMP-Anwendung, die auf Abfragen von SNMP-Manager-Anwendungen antwortet. Der SNMP-Agent ist für das Abrufen und Aktualisieren lokaler Verwaltungsinformationen basierend auf den Anforderungen des SNMP-Managers verantwortlich. Der Agent benachrichtigt auch registrierte Manager, wenn wichtige Ereignisse oder Traps auftreten. Ein Manager ist eine SNMP-Anwendung, die Abfragen für SNMP-Agent-Anwendungen generiert und Traps von SNMP-Agent-Anwendungen empfängt.

Auf Computern, auf denen Microsoft Windows XP/Windows 2000/Windows NT ausgeführt wird, wird der SNMP-Agent vom SNMP-Dienst (SNMP.EXE) implementiert. Der SNMP-Manager ist in der Regel eine SNMP-Verwaltungs Konsolenanwendung eines Drittanbieters. Die Verwaltungs Konsolenanwendung muss nicht auf demselben Host wie der SNMP-Agent ausgeführt werden. Um die Informationen zu verwenden, die der Microsoft SNMP-Dienst bereitstellt, benötigen Sie mindestens eine SNMP-Verwaltungs Konsolenanwendung. Das System enthält Bibliotheken, die SNMP-Verwaltungs Konsolen Anwendungen unterstützen. zurzeit ist jedoch keine SNMP-Verwaltungs Konsolenanwendung enthalten.

 

 