---
title: Allgemeine WinSNMP-Fehler Codes
description: Die snmpgetlasterror-Funktion kann einen allgemeinen Fehlercode zurückgeben, nachdem bei einer WinSNMP-Funktion ein Fehler aufgetreten ist. In der folgenden Tabelle sind die allgemeinen WinSNMP-Fehlercodes aufgeführt.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beee49aef651784b0b8dc05c0114b7bf906be113
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039324"
---
# <a name="winsnmp-common-error-codes"></a>Allgemeine WinSNMP-Fehler Codes

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion kann einen allgemeinen Fehlercode zurückgeben, nachdem bei einer WinSNMP-Funktion ein Fehler aufgetreten ist. In der folgenden Tabelle sind die allgemeinen WinSNMP-Fehlercodes aufgeführt.



| Fehlercode                | Bedeutung                                                                                                                                                                                                        | Empfohlene Maßnahme                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Snmpapi wurde \_ nicht \_ initialisiert. | Die [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion konnte nicht erfolgreich abgeschlossen werden, weil die Ausführung des Programms begonnen hat, oder weil ein Rückruf der [**snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) -Funktion erfolgreich abgeschlossen wurde. | Die Anwendung sollte [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) aufrufen, bevor Sie eine andere WinSNMP-API-Funktion aufruft, wenn [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) fehlschlägt. Die [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) -Funktion gibt erweiterte Fehlerinformationen zum Ausfall von [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)zurück.                                                          |
| Fehler bei Snmpapi- \_ Zuweisung. \_     | Die Anwendung hat einen ungültigen Zeiger angegeben, oder es ist ein Fehler bei der Speicher Belegung aufgetreten. Die Microsoft WinSNMP-Implementierung konnte nicht genügend Ressourcen zum Ausführen der Anforderung abrufen.                | Die Anwendung sollte gültige Speicher Zeiger für alle Ausgabeparameter bereitstellen. Er sollte Ressourcen freigeben, Ressourcenanforderungen reduzieren oder ein ordnungsgemäßes Herunterfahren vereinfachen. Ein ordnungsgemäßes Herunterfahren umfasst mehrere Aufrufe der [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion, eine für jede geöffnete WinSNMP-Sitzung. Außerdem ist ein aufrufsvorgang der [**snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) -Funktion enthalten. |
| Snmpapi- \_ NoOp             | Die Funktion wurde nicht erfolgreich abgeschlossen, weil alle Ausgabeparameter **null** sind.                                                                                                                         | Die Anwendung muss mindestens einen Ausgabeparameter angeben, der nicht **null** ist, wenn eine Funktion aufgerufen wird, die Informationen an die Anwendung zurückgibt.                                                                                                                                                                                                                                  |
| Snmpapi \_ - \_ Fehler     | Unbekannter oder nicht definierter Fehler.                                                                                                                                                                        | Die Anwendung sollte in der Regel mit einem ordnungsgemäßen Herunterfahren Antworten. Ein ordnungsgemäßes Herunterfahren umfasst mehrere Aufrufe der [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion, eine für jede geöffnete WinSNMP-Sitzung. Außerdem ist ein aufrufsvorgang der [**snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) -Funktion enthalten.                                                                                                           |



 

Die WinSNMP-Fehler, die kontextspezifische Informationen übermitteln, werden auf der Referenzseite der einzelnen Funktionen angegeben.

 

 