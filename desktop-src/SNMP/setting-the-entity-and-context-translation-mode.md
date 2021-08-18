---
title: Festlegen des Entitäts- und Kontextübersetzungsmodus
description: Die WinSNMP-Anwendung kann die Interpretation und Übersetzung von Entitäts- und Kontextparametern angeben, indem der Entitäts- und Kontextübersetzungsmodus festgelegt wird. Die Microsoft WinSNMP-Implementierung speichert den Modus in einer Datenbank.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab459c0b33ffe1cc43c81858b57ec55942f61f2b5b736ca0124f31f52cc960d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009058"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Festlegen des Entitäts- und Kontextübersetzungsmodus

Die WinSNMP-Anwendung kann die Interpretation und Übersetzung von Entitäts- und Kontextparametern angeben, indem der Entitäts- und Kontextübersetzungsmodus festgelegt wird. Die Microsoft WinSNMP-Implementierung speichert den Modus in einer Datenbank.

Die Einstellung des Entitäts- und Kontextübersetzungsmodus bestimmt die Art und Weise, in der die [**SnmpStrToEntity-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) und die [**SnmpStrToContext-Funktion Eingabezeichenfolgen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretieren. Die Einstellung bestimmt auch den Typ der Ausgabezeichenfolge, die die [**Funktionen SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) und [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) zurückgeben. Weitere Informationen finden Sie unter [Unterstützung für IPX-Adresszeichenfolgen in WinSNMP.](support-for-ipx-address-strings-in-winsnmp.md)

Die Implementierung gibt die aktuelle Standardentität und den Kontextübersetzungsmodus im *nTranslateMode-Parameter* der [**SnmpStartup-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) zurück. Um die aktuelle Entität und den Kontextübersetzungsmodus abzurufen, die für die Implementierung wirksam sind, kann eine Anwendung jederzeit die [**SnmpGetTranslateMode-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) aufrufen.

Die gültigen Entitäts- und Kontextübersetzungsmodi folgen.

| Mode                      | Bedeutung                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ ÜBERSETZT       | Die Implementierung verwendet ihre Datenbank, um benutzerfreundliche Namen für SNMP-Entitäten und verwaltete Objekte zu übersetzen. Die Implementierung übersetzt sie in ihre SNMPv1- oder SNMPv2C-Komponenten.                                                                                                  |
| SNMPAPI \_ UNTRANSLATED \_ V1 | Die Implementierung interpretiert SNMP-Entitätsparameter als literale SNMP-Transportadressen und Kontextparameter als literale SNMP-Communityzeichenfolgen. Für SNMPv2-Zielentitäten erstellt die Implementierung ausgehende SNMP-Nachrichten, die den Wert 0 (null) im Versionsfeld enthalten. |
| SNMPAPI \_ UNTRANSLATED \_ V2 | Die Implementierung interpretiert SNMP-Entitätsparameter als SNMP-Transportadressen und Kontextparameter als literale SNMP-Communityzeichenfolgen. Für SNMPv2-Zielentitäten erstellt die Implementierung ausgehende SNMP-Nachrichten, die den Wert 1 im Versionsfeld enthalten.            |



 

Die Implementierung versucht, Ressourcen in ihrer Datenbank der Literaltransportadresse der Verwaltungsentität zu zuordnen.

Um die Einstellung des Entitäts- und Kontextübersetzungsmodus zu ändern, muss eine WinSNMP-Anwendung die [**SnmpSetTranslateMode-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) aufrufen. Wenn der angeforderte Übersetzungsmodus ungültig ist, schlägt die Funktion fehl, und [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) gibt den Fehlercode SNMPAPI \_ MODE INVALID \_ zurück.

 

 




