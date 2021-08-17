---
title: WinSNMP-Fehlercodes
description: WinSNMP-Fehlercodes
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP-Fehlercodes SNMP
- Fehlercodes SNMP , WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2a9f9dda792008a0e69e6c23e692b4aa4c4e78316eeca015f7b056e2a275df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142863"
---
# <a name="winsnmp-error-codes"></a>WinSNMP-Fehlercodes

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

> [!Note]  
> Die in diesem Thema beschriebenen Fehler unterscheiden sich von den von den relevanten RFCs definierten SNMP-Fehlercodes.

 

Alle WinSNMP-Funktionen geben den Wert **SNMPAPI \_ FAILURE** zurück, wenn die Funktion fehlschlägt. Die WinSNMP-Anwendung muss sofort die [**SnmpGetLastError-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) aufrufen, um erweiterte Fehlerinformationen abzurufen, wenn bei einer WinSNMP-Funktion ein Fehler auftritt. Die folgende Tabelle enthält Themen, in denen erweiterte Fehlercodes behandelt werden, die von WinSNMP-Funktionen zurückgegeben werden.



| Thema                                                        | Beschreibung                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Allgemeine WinSNMP-Fehlercodes](winsnmp-common-error-codes.md) | Beschreibt allgemeine Fehlercodes für die WinSNMP-API.       |
| [Netzwerktransportfehler](network-transport-errors.md)     | Beschreibt Netzwerktransportfehler für die WinSNMP-API. |



 

Die WinSNMP-Fehler, die kontextspezifische Informationen vermitteln, sind auf der Funktionsverweisseite enthalten.

 

 