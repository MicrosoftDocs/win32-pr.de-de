---
title: SNMP-Variablen Typen und PDU-Anforderungs Typen
description: Die Definitionen für einige SNMP-Variablen Typen und PDU-Anforderungs Typen wurden geändert. Die Datei SNMP. h ordnet alte Typen den entsprechenden neuen Typen zu.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728953"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>SNMP-Variablen Typen und PDU-Anforderungs Typen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die Definitionen für einige SNMP-Variablen Typen und PDU-Anforderungs Typen wurden geändert. Die Datei SNMP. h ordnet alte Typen den entsprechenden neuen Typen zu.

## <a name="modified-snmp-variable-types"></a>Geänderte SNMP-Variablen Typen

Sie sollten die neuen SNMP-Variablen Typen verwenden, die in der folgenden Tabelle aufgeführt sind, wenn Sie Manager-Anwendungen entwickeln, die die Microsoft SNMP-Verwaltungs-API verwenden. In der Tabelle werden die alten SNMP-Variablen Typen mit den entsprechenden neuen Variablen Typen aufgelistet.

| Alter Variablentyp        | Neuer Variablentyp |
|--------------------------|-------------------|
| ASN \_ RFC1155 \_ IPAddress  | ASN- \_ IPAddress    |
| ASN \_ RFC1155- \_ Counter    | ASN \_ COUNTER32    |
| ASN \_ RFC1155 \_ Messgerät      | ASN \_ GAUGE32      |
| ASN \_ RFC1155 \_ TimeTicks  | ASN- \_ TimeTicks    |
| ASN \_ RFC1155 nicht transparent \_     | ASN \_ nicht transparent       |
| ASN \_ RFC1213 \_ dispstring | ASN \_ octetstring  |



 

## <a name="modified-snmp-pdu-request-types"></a>Geänderte SNMP-PDU-Anforderungs Typen

Sie sollten die neuen SNMP-PDU-Typen verwenden, die in der folgenden Tabelle aufgeführt sind, wenn Sie Manager-Anwendungen entwickeln, die die Microsoft SNMP-Verwaltungs-API verwenden. In der Tabelle sind die alten SNMP-PDU-Typen mit den entsprechenden neuen PDU-Typen aufgeführt.

| Alter PDU-Typ                 | Neuer PDU-Typ        |
|------------------------------|---------------------|
| ASN \_ RFC1157 \_ GetRequest     | SNMP \_ PDU \_ Get      |
| ASN \_ RFC1157 \_ getnextrequest | SNMP \_ PDU \_ GetNext  |
| ASN \_ RFC1157 \_ GetResponse    | SNMP- \_ PDU- \_ Antwort |
| ASN \_ RFC1157 \_ abtrequest     | SNMP- \_ PDU- \_ Satz      |
| ASN \_ RFC1157 \_ Trap           | SNMP \_ PDU \_ V1TRAP   |



 

 

 