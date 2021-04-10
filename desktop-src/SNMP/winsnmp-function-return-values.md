---
title: Rückgabewerte der WinSNMP-Funktion
description: Der Rückgabewert eines WinSNMP-Funktions Aufrufes kann ein Handle für eine Ressource sein, die von der Microsoft WinSNMP-Implementierung für die WinSNMP-Anwendung zugewiesen wird.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039484"
---
# <a name="winsnmp-function-return-values"></a>Rückgabewerte der WinSNMP-Funktion

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Der Rückgabewert eines WinSNMP-Funktions Aufrufes kann ein Handle für eine Ressource sein, die von der Microsoft WinSNMP-Implementierung für die WinSNMP-Anwendung zugewiesen wird.

In der folgenden Tabelle werden die fünf Typen von Ressourcen Handles aufgelistet, die von der-Implementierung zugewiesen werden.



| Handle-Typ    | BESCHREIBUNG                       |
|----------------|-----------------------------------|
| hsnmp- \_ Sitzung | Handle für eine WinSNMP-Sitzung       |
| hsnmp- \_ Entität  | Handle für eine SNMP-Entität          |
| hsnmp- \_ Kontext | Handle für einen SNMP-Kontext         |
| hsnmp- \_ PDU     | Handle für eine Protokolldaten Einheit    |
| hsnmp- \_ VBL     | Handle für eine Variablen Bindungs Liste |



 

Weitere Informationen finden Sie unter [Ressourcenhandle-Objekte](resource-handle-objects.md).

Der Rückgabewert kann auch ein Ganzzahl ohne Vorzeichen Long Integer-Wert des **smiUINT32** -Typs sein, der einen Snmpapi- \_ Status Wert darstellt.

In der folgenden Tabelle sind die WinSNMP-Statuswerte und ihre Bedeutung aufgeführt.



| Status           | BESCHREIBUNG                                                                      |
|------------------|----------------------------------------------------------------------------------|
| Snmpapi- \_ Fehler | Gibt einen Fehler an. Entspricht 0 oder **null**.                                    |
| Snmpapi- \_ Erfolg | Gibt an, dass die Funktion erfolgreich abgeschlossen wurde. Entspricht 1 oder einer positiven Anzahl. |



 

 

 