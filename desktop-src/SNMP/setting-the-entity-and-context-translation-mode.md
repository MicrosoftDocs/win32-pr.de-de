---
title: Festlegen des Entitäts-und Kontext Übersetzungsmodus
description: Die WinSNMP-Anwendung kann die Interpretation und Übersetzung von Entitäts-und Kontext Parametern angeben, indem der Entitäts-und Kontext Übersetzungsmodus festgelegt wird. Die Microsoft WinSNMP-Implementierung speichert den Modus in einer-Datenbank.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036665"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Festlegen des Entitäts-und Kontext Übersetzungsmodus

Die WinSNMP-Anwendung kann die Interpretation und Übersetzung von Entitäts-und Kontext Parametern angeben, indem der Entitäts-und Kontext Übersetzungsmodus festgelegt wird. Die Microsoft WinSNMP-Implementierung speichert den Modus in einer-Datenbank.

Die Einstellung des Entitäts-und Kontext Übersetzungsmodus bestimmt die Art und Weise, wie die [**snmpstrto Entity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) -Funktion und die [**snmpstrdecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) -Funktion Eingabe Zeichenfolgen interpretieren. Die-Einstellung bestimmt auch den Typ der Ausgabe Zeichenfolge, die die [**snmpentityrestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) -Funktion und die [**snmpcontextdestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) -Funktion zurückgeben. Weitere Informationen finden Sie [unter Unterstützung für IPX-Adress Zeichenfolgen in WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).

Die-Implementierung gibt den aktuellen Standard Entitäts-und Kontext Übersetzungsmodus im *ntranslatemode* -Parameter der [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion zurück. Zum Abrufen des aktuellen Entitäts-und Kontext Übersetzungsmodus, der für die Implementierung wirksam ist, kann eine Anwendung die [**snmpgettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) -Funktion jederzeit aufrufen.

Die gültigen Entitäts-und Kontext Übersetzungs Modi folgen.

| Mode                      | Bedeutung                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Snmpapi \_ übersetzt       | Die-Implementierung verwendet die Datenbank, um benutzerfreundliche Namen für SNMP-Entitäten und verwaltete Objekte zu übersetzen. Die-Implementierung übersetzt Sie in Ihre SNMPv1-oder SNMPv2C-Komponenten.                                                                                                  |
| Snmpapi \_ nicht übersetzt \_ v1 | Die-Implementierung interpretiert SNMP-Entitäts Parameter als Literale SNMP-Transport Adressen und Kontext Parameter als Literale SNMP-Communityzeichenfolgen. Für SNMPv2-Ziel Entitäten erstellt die-Implementierung ausgehende SNMP-Nachrichten, die den Wert 0 (null) im Versions Feld enthalten. |
| Snmpapi \_ nicht übersetzt \_ v2 | Die-Implementierung interpretiert SNMP-Entitäts Parameter als SNMP-Transport Adressen und Kontext Parameter als Literale SNMP-Communityzeichenfolgen. Für SNMPv2-Ziel Entitäten erstellt die-Implementierung ausgehende SNMP-Nachrichten, die im Feld Version den Wert 1 enthalten.            |



 

Die-Implementierung versucht, Ressourcen in der Datenbank der literalen Transport Adresse der Verwaltungs Entität zuzuordnen.

Um die Einstellung für den Entitäts-und Kontext Übersetzungsmodus zu ändern, muss eine WinSNMP-Anwendung die [**snmpsettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) -Funktion aufrufen. Wenn der angeforderte Übersetzungsmodus ungültig ist, tritt bei der Funktion ein Fehler auf, und [**snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) gibt den Fehlercode "Snmpapi- \_ Modus ungültig" zurück \_ .

 

 




