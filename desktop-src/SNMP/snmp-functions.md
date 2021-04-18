---
title: SNMP-Funktionen
description: In diesem Thema werden drei Gruppierungen von SNMP-Funktionen beschrieben und die Funktionen aufgelistet, die in jeder Gruppe enthalten sind.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP-Funktionen (SNMP)
- Functions SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473973"
---
# <a name="snmp-functions"></a>SNMP-Funktionen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

In diesem Thema werden drei Gruppierungen von SNMP-Funktionen beschrieben und die Funktionen aufgelistet, die in jeder Gruppe enthalten sind:

-   [API-Funktionen des SNMP-Erweiterungs-Agents](#snmp-extension-agent-api-functions)
-   [SNMP-Verwaltungs-API-Funktionen](#snmp-management-api-functions)
-   [API-Funktionen der SNMP-Hilfsprogramme](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>API-Funktionen des SNMP-Erweiterungs-Agents

Die SNMP-Erweiterungs-Agent-Funktionen definieren die Schnittstelle zwischen dem SNMP-Dienst und den DLLs des Drittanbieter-SNMP-Erweiterungs-Agents. In der folgenden Tabelle sind Funktionen aufgeführt, mit denen Anwendungen Variablen Bindungen auflösen können, die von eingehenden SNMP-Protokolldaten Einheiten (PDUs) angegeben werden.

| API-Funktion des SNMP-Erweiterungs-Agents                    | BESCHREIBUNG                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**Snmpextensionclose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Fordert an, dass der SNMP-Erweiterungs-Agent Ressourcen aufhebt und Vorgänge beendet.                                    |
| [**Snmpextensioninit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Initialisiert die SNMP-Erweiterungs-Agent-dll.                                                                                |
| [**Snmpextensioninitex**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifiziert alle zusätzlichen MIB (Management Information Base)-Unterstrukturen, die der SNMP-Erweiterungs-Agent unterstützt.             |
| [**Snmpextensionmonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Bietet dem SNMP-Erweiterungs-Agent Informationen zu den internen Indikatoren und Parametern des Dienstanbieter.            |
| [**Snmpextensionquery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Löst SNMP-Anforderungen auf, die Variablen in mindestens einer der registrierten MIB-Teil Strukturen des SNMP-Erweiterungs-Agents enthalten. |
| [**Snmpextensionqueryex**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Verarbeitet SNMP-Anforderungen, die Variablen in mindestens einer MIB-Unterstruktur angeben, die von SNMP-Erweiterungs-Agents registriert werden. |
| [**Snmpextensiontrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Ruft Informationen ab, die der Dienst benötigt, um Traps für den SNMP-Erweiterungs-Agent zu generieren.                          |



 

## <a name="snmp-management-api-functions"></a>SNMP-Verwaltungs-API-Funktionen

Die SNMP-Verwaltungsfunktionen definieren die Schnittstelle zwischen SNMP-Manager-Anwendungen von Drittanbietern und der Verwaltungsfunktion Dynamic-Link Library (dll)-Mgmtapi.dll. Die dll funktioniert in Verbindung mit dem SNMP-Trap Dienst (Snmptrap.exe) und kann mit einer oder mehreren Drittanbieter Anwendungen von SNMP-Manager interagieren. In der folgenden Tabelle werden die Verwaltungsfunktionen aufgelistet, die von Drittanbieter Anwendungen zum Ausführen von SNMP-Manager-Vorgängen verwendet werden.

| SNMP-Verwaltungs-API-Funktion                   | BESCHREIBUNG                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Snmpmgrclose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Schließt die Kommunikations Sockets und Datenstrukturen, die der angegebenen Sitzung zugeordnet sind.                                                                                                  |
| [**Snmpmgrctl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Legt einen mit einer SNMP-Sitzung verknüpften Betriebsparameter fest.                                                                                                                                   |
| [**Snmpmgrgettrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Gibt ausstehende Trap Daten zurück, die der Aufrufer nicht empfangen hat, wenn der Trap-Empfang aktiviert ist.                                                                                                           |
| [**Snmpmgrgettrapex**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Gibt ausstehende Trap Daten zurück, die der Aufrufer nicht empfangen hat, wenn der Trap-Empfang aktiviert ist. Gibt auch die Adresse der transportquelle und des Community-Traps zurück, die dem Trap zugeordnet ist. |
| [**Snmpmgroidin**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Konvertiert eine interne objektbezeichnerstruktur in ihre Zeichen folgen Darstellung.                                                                                                                         |
| [**Snmpmgropen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Initialisiert Kommunikations Sockets und Datenstrukturen, die für die Herstellung der Kommunikation mit dem SNMP-Agent erforderlich sind.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Fordert an, dass der angegebene Vorgang vom angegebenen Agent ausgeführt wird.                                                                                                                             |
| [**Snmpmgrotesoid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Konvertiert das Zeichen folgen Format eines Objekt Bezeichners in die interne objektbezeichnerstruktur.                                                                                                        |
| [**Snmpmgrtraplauschen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registriert die Fähigkeit einer SNMP-Manager-Anwendung, SNMP-Traps vom SNMP-Trap Dienst zu empfangen.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>API-Funktionen der SNMP-Hilfsprogramme

Die SNMP-Dienstprogramm Funktionen stellen Funktionen bereit, die während der Entwicklung von SNMP-Anwendungen nützlich sind, einschließlich der Vereinfachung der Bearbeitung von SNMP-Datenstrukturen. In der folgenden Tabelle sind die Funktionen des SNMP-Hilfsprogramms aufgeführt.

| SNMP-Hilfsprogramm-API                                  | BESCHREIBUNG                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Snmpsvcgetuptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Ruft die Zeit in Minuten ab, für die der SNMP-Dienst ausgeführt wurde.                                                                                  |
| [**Snmpsvcsetloglevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Passt die Detailebene der Debugausgabe vom SNMP-Dienst und von SNMP-Erweiterungs-Agents an.                                                              |
| [**Snmpsvcsetlogtype**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Passt das Ziel für die Debugausgabe vom SNMP-Dienst und von SNMP-Erweiterungs-Agents an.                                                                 |
| [**Snmputilasnanycpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Kopiert eine Quell- [**asnany**](/windows/desktop/api/Snmp/ns-snmp-asnany) -Struktur in eine **asnany** -Zielstruktur.                                                                      |
| [**Snmputilasnanyfree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Gibt den Arbeitsspeicher frei, der für eine angegebene [**asnany**](/windows/desktop/api/Snmp/ns-snmp-asnany) -Struktur reserviert wurde.                                                                        |
| [**Snmputildbgprint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Legt die Ebene der Debuginformationen fest, die vom SNMP-Dienst oder von einem [**snmputildbgprint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)-Rückruf empfangen werden sollen.                       |
| [**Snmputilidstoa**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Konvertiert einen Objekt Bezeichner (OID) in eine NULL-terminierte Zeichenfolge.                                                                                                   |
| [**Snmputilmemzuweisung**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Weist dynamischen Arbeitsspeicher aus dem Prozess Heap zu.                                                                                                                    |
| [**Snmputilmemfree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Gibt das angegebene Speicher Objekt frei.                                                                                                                                 |
| [**Snmputilmemrezuweisungen**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Ändert die Größe des angegebenen Speicher Objekts.                                                                                                                   |
| [**Snmputiloctetscmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Vergleicht zwei Oktett-Zeichen folgen.                                                                                                                                        |
| [**Snmputiloctetscpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Kopiert eine [**asnoctetstring**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) -Quell Struktur in eine **asnoctetstring** -Zielstruktur.                                              |
| [**Snmputilocteout**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Gibt den Arbeitsspeicher frei, der für die angegebene Oktett-Zeichenfolge reserviert wurde.                                                                                                |
| [**Snmputiloctetincmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Führt einen Vergleich von zwei Oktett-Zeichen folgen mit der angegebenen Anzahl von unter Elementen aus.                                                                              |
| [**Snmputiloidappend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Fügt einen Quell Objekt Bezeichner, der in einer [**asnobjectidentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) -Struktur enthalten ist, an einen Zielobjekt Bezeichner an.          |
| [**Snmputiloidcmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Vergleicht zwei Objekt Bezeichner, die in [**asnobjectidentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) -Strukturen enthalten sind.                                           |
| [**Snmputiloidcpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Kopiert eine Quell- [**asnobjectidentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) -Struktur in eine **asnobjectidentifier** -Zielstruktur.                               |
| [**Snmputiloidfree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Gibt den Arbeitsspeicher frei, der für den angegebenen Objekt Bezeichner zugeordnet wurde.                                                                                           |
| [**Snmputiloidncmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Vergleicht zwei Objekt Bezeichner, die in [**asnobjectidentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) -Strukturen enthalten sind, mit der angegebenen Anzahl von subidentifiers. |
| [**Snmputiloiddienst**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Konvertiert einen Objekt Bezeichner (OID) in eine NULL-terminierte Zeichenfolge.                                                                                                   |
| [**Snmputilprintasnany**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Druckt einen Wert, der in einer [**asnany**](/windows/desktop/api/Snmp/ns-snmp-asnany) -Struktur zu Debuggen und zu Entwicklungszwecken enthalten ist.                                              |
| [**Snmputilprintoid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formatiert den angegebenen Objekt Bezeichner (OID) und druckt das Ergebnis auf das Standardausgabe Gerät.                                                                 |
| [**Snmputilvarbindcpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Kopiert eine [**snmpvarbind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) -Quell Struktur in eine **snmpvarbind** -Zielstruktur.                                                       |
| [**Snmputilvarbindlistcpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Kopiert eine [**snmpvarbindlist**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) -Quell Struktur in eine Ziel- **snmpvarbindlist** -Struktur.                                           |
| [**Snmputilvarbindfree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Gibt den Arbeitsspeicher frei, der für die angegebene [**snmpvarbind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) -Struktur reserviert wurde.                                                            |
| [**Snmputilvarbindlistfree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Gibt den Arbeitsspeicher frei, der für die angegebene [**snmpvarbindlist**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) -Struktur reserviert wurde.                                                    |



 

 

 