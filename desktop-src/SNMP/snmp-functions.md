---
title: SNMP-Funktionen
description: In diesem Thema werden drei Gruppierungen von SNMP-Funktionen beschrieben und die funktionen aufgeführt, die in jeder Gruppe enthalten sind.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP Functions SNMP
- Funktionen SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42028e4045d4d0dfeb183dc29a3dc85e7220ed3d5bccf39a3cc9871215188153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143013"
---
# <a name="snmp-functions"></a>SNMP-Funktionen

\[SNMP ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung,](/windows/desktop/WinRM/portal)bei der es sich um die Microsoft-Implementierung von WS-Man handelt.\]

In diesem Thema werden drei Gruppierungen von SNMP-Funktionen beschrieben und die Funktionen aufgeführt, die in jeder Gruppe enthalten sind:

-   [API-Funktionen des SNMP-Erweiterungs-Agents](#snmp-extension-agent-api-functions)
-   [SNMP-Verwaltungs-API Funktionen](#snmp-management-api-functions)
-   [API-Funktionen des SNMP-Hilfsprogramms](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>API-Funktionen des SNMP-Erweiterungs-Agents

Die Funktionen des SNMP-Erweiterungs-Agents definieren die Schnittstelle zwischen dem SNMP-Dienst und den DLLs des SNMP-Erweiterungs-Agents von Drittanbietern. In der folgenden Tabelle sind Funktionen aufgeführt, mit denen Anwendungen Variablenbindungen auflösen können, die von eingehenden SNMP-Protokolldateneinheiten (PDUs) angegeben werden.

| API-Funktion des SNMP-Erweiterungs-Agents                    | Beschreibung                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Fordert an, dass der SNMP-Erweiterungs-Agent die Ressourcen zu einem anderen Konto befindt und Vorgänge beendet.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Initialisiert die DLL des SNMP-Erweiterungs-Agents.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifiziert alle zusätzlichen MIB-Teilstruktur (Management Information Base), die der SNMP-Erweiterungs-Agent unterstützt.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Stellt dem SNMP-Erweiterungs-Agent Informationen zu den internen Leistungsindikatoren und Parametern des Diensts zur Verfügung.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Löst SNMP-Anforderungen auf, die Variablen in einer oder mehr der registrierten MIB-Teilstruktur des SNMP-Erweiterungs-Agents enthalten. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Verarbeitet SNMP-Anforderungen, die Variablen in mindestens einer MIB-Teilstruktur angeben, die von SNMP-Erweiterungs-Agents registriert werden. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Ruft Informationen ab, die der Dienst zum Generieren von Traps für den SNMP-Erweiterungs-Agent benötigt.                          |



 

## <a name="snmp-management-api-functions"></a>SNMP-Verwaltungs-API Funktionen

Die SNMP-Verwaltungsfunktionen definieren die Schnittstelle zwischen SNMP-Manager-Anwendungen von Drittanbietern und der DLL-Mgmtapi.dll. Die DLL funktioniert in Verbindung mit dem SNMP-Trapdienst (Snmptrap.exe) und kann mit einer oder mehrere SNMP-Manager-Anwendungen von Drittanbietern interagieren. In der folgenden Tabelle sind die Verwaltungsfunktionen aufgeführt, die Manager-Anwendungen von Drittanbietern zum Ausführen von SNMP-Managervorgängen verwenden.

| SNMP-Verwaltungs-API Funktion                   | Beschreibung                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Schließt die Kommunikationssockes und Datenstrukturen, die der angegebenen Sitzung zugeordnet sind.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Legt einen Betriebsparameter fest, der einer SNMP-Sitzung zugeordnet ist.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Gibt ausstehende Trapdaten zurück, die der Aufrufer nicht empfangen hat, wenn der Trapempfang aktiviert ist.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Gibt ausstehende Trapdaten zurück, die der Aufrufer nicht empfangen hat, wenn der Trapempfang aktiviert ist. Gibt auch die Adresse der Transportquelle und den Community-Trap zurück, der dem Trap zugeordnet ist. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Konvertiert eine interne Objektbezeichnerstruktur in ihre Zeichenfolgendarstellung.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Initialisiert Kommunikationssockets und Datenstrukturen, die zum Herstellen der Kommunikation mit dem SNMP-Agent erforderlich sind.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Fordert an, dass der angegebene Vorgang vom angegebenen Agent ausgeführt wird.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Konvertiert das Zeichenfolgenformat eines Objektbezeichners in seine interne Objektbezeichnerstruktur.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registriert die Fähigkeit einer SNMP-Manager-Anwendung, SNMP-Traps vom SNMP-Trapdienst zu empfangen.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>API-Funktionen des SNMP-Hilfsprogramms

Die SNMP-Hilfsfunktionen bieten Funktionen, die bei der Entwicklung von SNMP-Anwendungen nützlich sind, einschließlich der Vereinfachung der Bearbeitung von SNMP-Datenstrukturen. In der folgenden Tabelle sind die Funktionen des SNMP-Hilfsprogramms aufgeführt.

| API-Funktion des SNMP-Hilfsprogramms                                  | Beschreibung                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Ruft die Zeit in Millisekunden ab, für die der SNMP-Dienst ausgeführt wurde.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Passt die Detailebene der Debugausgabe des SNMP-Diensts und der SNMP-Erweiterungs-Agents an.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Passt das Ziel für die Debugausgabe des SNMP-Diensts und der SNMP-Erweiterungs-Agents an.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Kopiert eine [**AsnAny-Quellstruktur**](/windows/desktop/api/Snmp/ns-snmp-asnany) in eine **AsnAny-Zielstruktur.**                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Gibt den Arbeitsspeicher frei, der für eine angegebene [**AsnAny-Struktur zugeordnet**](/windows/desktop/api/Snmp/ns-snmp-asnany) wurde.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Legt die Ebene der Debuginformationen fest, die vom SNMP-Dienst oder von einem Aufruf von [**SnmpUtilDbgPrint empfangen werden sollen.**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Konvertiert einen Objektbezeichner (OID) in eine auf NULL beendete Zeichenfolge.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Weist dynamischen Arbeitsspeicher aus dem Prozesshap zu.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Gibt das angegebene Speicherobjekt frei.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Ändert die Größe des angegebenen Speicherobjekts.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Vergleicht zwei Oktettzeichenfolgen.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Kopiert eine [**AsnOctetString-Quellstruktur**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) in eine **AsnOctetString-Zielstruktur.**                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Gibt den Arbeitsspeicher frei, der für die angegebene Oktettzeichenfolge zugeordnet wurde.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Führt einen Vergleich von zwei Oktettzeichenfolgen mit der angegebenen Anzahl von Unteridentifizierern aus.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Fügt einen Quellobjektbezeichner, der in einer [**AsnObjectIdentifier-Struktur**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) enthalten ist, an einen Zielobjektbezeichner an.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Vergleicht zwei Objektbezeichner, die in [**AsnObjectIdentifier-Strukturen enthalten**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) sind.                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Kopiert eine [**AsnObjectIdentifier-Quellstruktur**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) in eine **AsnObjectIdentifier-Zielstruktur.**                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Gibt den Arbeitsspeicher frei, der für den angegebenen Objektbezeichner zugeordnet wurde.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Vergleicht zwei Objektbezeichner, die in [**AsnObjectIdentifier-Strukturen**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) enthalten sind, mit der angegebenen Anzahl von Unteridentifizierern. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Konvertiert einen Objektbezeichner (OID) in eine auf NULL endende Zeichenfolge.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Gibt einen Wert aus, der in einer [**AsnAny-Struktur**](/windows/desktop/api/Snmp/ns-snmp-asnany) für Debug- und Entwicklungszwecke enthalten ist.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formatiert den angegebenen Objektbezeichner (OID) und gibt das Ergebnis auf dem Standardausgabegerät aus.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Kopiert eine [**SnmpVarBind-Quellstruktur**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) in eine **SnmpVarBind-Zielstruktur.**                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Kopiert eine [**SnmpVarBindList-Quellstruktur**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) in eine **SnmpVarBindList-Zielstruktur.**                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Gibt den Arbeitsspeicher frei, der für die angegebene [**SnmpVarBind-Struktur**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) zugeordnet wurde.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Gibt den Arbeitsspeicher frei, der für die angegebene [**SnmpVarBindList-Struktur**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) zugeordnet wurde.                                                    |



 

 

 