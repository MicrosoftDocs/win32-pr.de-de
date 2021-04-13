---
title: WinSNMP-Fehler Codes
description: WinSNMP-Fehler Codes
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP-Fehler Codes SNMP
- Fehler Codes SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473965"
---
# <a name="winsnmp-error-codes"></a>WinSNMP-Fehler Codes

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

> [!Note]  
> Die in diesem Thema beschriebenen Fehler unterscheiden sich von den SNMP-Fehlercodes, die von den entsprechenden RFCs definiert werden.

 

Alle WinSNMP-Funktionen geben den Wert **Snmpapi \_ Failure** zurück, wenn die Funktion fehlschlägt. Die WinSNMP-Anwendung muss sofort die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion aufrufen, um erweiterte Fehlerinformationen abzurufen, wenn eine WinSNMP-Funktion fehlschlägt. Die folgende Tabelle enthält Themen, in denen die von WinSNMP-Funktionen zurückgegebenen erweiterten Fehlercodes erläutert werden.



| Thema                                                        | BESCHREIBUNG                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Allgemeine WinSNMP-Fehler Codes](winsnmp-common-error-codes.md) | Beschreibt häufige Fehlercodes für die WinSNMP-API.       |
| [Netzwerk Transport Fehler](network-transport-errors.md)     | Beschreibt Netzwerk Transport Fehler für die WinSNMP-API. |



 

Die WinSNMP-Fehler, die kontextspezifische Informationen übermitteln, sind auf der Seite Funktionsreferenz enthalten.

 

 