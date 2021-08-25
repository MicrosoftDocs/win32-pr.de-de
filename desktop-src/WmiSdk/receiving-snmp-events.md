---
description: Die SNMP-Ereignisanbieter unterstützen SNMPv1-Traps und SNMPv2-Benachrichtigungen.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Empfangen von SNMP-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf09e32ec05d42adcc60891cd369cde1f3f078541416ce1a492484de024744bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996020"
---
# <a name="receiving-snmp-events"></a>Empfangen von SNMP-Ereignissen

Die SNMP-Ereignisanbieter unterstützen SNMPv1-Traps und SNMPv2-Benachrichtigungen.

Die folgenden drei Typen von SNMPv1-Traps und SNMPv2-Benachrichtigungen werden unterstützt:

-   Allgemein

    Generische Traps und Benachrichtigungen entsprechen benannten Ereignissen wie Linkup und Kaltstart. Generische Traps und Benachrichtigungen werden durch Klassen wie **SnmpLinkUpNotification** und **SnmpWarmStartExtendedNotification** dargestellt, die den Namen des Traps im Klassennamen enthalten. Diese Klassen sind Unterklassen von [SnmpNotification](snmpnotification.md) und [SnmpExtendedNotification.](snmpextendednotification.md)

-   Enterprise spezifisch

    Enterprise bestimmten Traps und Benachrichtigungen entsprechen Ereignissen, die durch eine WMI-Klasse dargestellt werden, die keine Unterklasse von [SnmpNotification](snmpnotification.md) und [SnmpExtendedNotification](snmpextendednotification.md)ist. Um unternehmensspezifische Traps und Benachrichtigungen zu unterstützen, muss ein Consumer Klassen durch Kompilieren von MIB-Definitionen mit dem SNMP MIB-Compiler definieren.

-   Enterprise nicht spezifisch

    Nicht unternehmensspezifische Traps und Benachrichtigungen entsprechen keinem der generischen Ereignistypen oder unternehmensspezifischen Ereignistypen. Für nicht unternehmensspezifische Traps und Benachrichtigungen wurden die MIB-Definitionen nicht im SMIR kompiliert. Sie werden durch die Klassen [SnmpNotification,](snmpnotification.md) **SnmpV2Notification,** **SnmpV1ExtendedNotification** und **SnmpV2ExtendedNotification** dargestellt, die von SnmpNotification und [SnmpExtendedNotification](snmpextendednotification.md)abgeleitet werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Empfangen generischer SNMP-Ereignisse](#receiving-generic-snmp-events)
-   [Empfangen von Enterprise-Specific Ereignissen](#receiving-enterprise-specific-events)
-   [Empfangen von Enterprise-Nonspecific Ereignissen](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Empfangen generischer SNMP-Ereignisse

SEEP und SREP unterstützen alle Typen generischer SNMPv1-Traps und SNMPv2-Benachrichtigungen. Generische SNMP-Ereignisse werden durch Unterklassen der Klassen [SnmpNotification](snmpnotification.md) und [SnmpExtendedNotification](snmpextendednotification.md) dargestellt.

Jeder Ereignistyp wird durch eine SEEP-Klasse und eine SREP-Klasse dargestellt. Die SEEP-Klassen werden von [SnmpNotification](snmpnotification.md)abgeleitet. Die SREP-Klassen werden von [SnmpExtendedNotification](snmpextendednotification.md)abgeleitet. Die Ereignisanbieter erfordern unterschiedliche Klassen, da sie bei der Darstellung der SNMP-Ereignisdaten unterschiedliche Mechanismen verwenden.

SeeP konvertiert die SNMP-Ereignisdaten direkt in WMI-Klasseneigenschaften, während dies bei SREP nicht der Fall ist. SREP fügt der Interpretation, die für die Verwendung der WMI-Eigenschaften erforderlich ist, eine Dekonstruktionsebene hinzu. Die Eigenschaften der [SNMPExtendedNotification-Unterklassen](snmpextendednotification.md) sind Instanzen von SNMP-Klassen. Die Eigenschaften der SEEP [SnmpNotification-Unterklassen](snmpnotification.md) sind ganze Zahlen und Zeichenfolgen.

In der folgenden Tabelle sind die Typen generischer SNMP-Ereignisse und die zugeordneten Ereignisklassen aufgeführt.



| SNMP-Ereignis                                    | SEEP-Klasse                                | SREP-Klasse                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Authentifizierungsfehler                        | **SnmpAuthenticationFailureNotification** | **SnmpAuthenticationFailureExtendedNotification** |
| Nachbarverlust des äußeren Gatewayprotokolls (EGP) | **SnmpEGPNeighborLossNotification**       | **SnmpEGPNeighborLossExtendedNotification**       |
| Kaltstart                                    | **SnmpColdStartNotification**             | **SnmpColdStartExtendedNotification**             |
| Warmer Start                                    | **SnmpWarmStartNotification**             | **SnmpWarmStartExtendedNotification**             |
| Verknüpfen                                       | **SnmpLinkUpNotification**                | **SnmpLinkUpExtendedNotification**                |
| Link nach unten                                     | **SnmpLinkDownNotification**              | **SnmpLinkDownExtendedNotification**              |



 

Beispielsweise beschreiben die Klassen **SnmpLinkUpNotification** und **SnmpLinkUpExtendedNotification** das Linkupereignis. Beide Klassen enthalten die Eigenschaften **ifIndex**, **ifAdminStatus** und **ifOperStatus,** weisen jedoch sehr unterschiedliche Typen auf. Die Eigenschaften in der **SnmpLinkUpNotification-Klasse** sind vom Typ SINT32 und STRING. Die Eigenschaften in der **SnmpLinkUpExtendedNotification-Klasse** sind der eingebettete Objekttyp IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable.

## <a name="receiving-enterprise-specific-events"></a>Empfangen von Enterprise-Specific Ereignissen

SEEP und SREP unterstützen alle unternehmensspezifischen Traps und Benachrichtigungen, die Sie im SMIR kompiliert haben.

Im folgenden Verfahren wird beschrieben, wie unternehmensspezifische Ereignisse empfangen werden.

**So empfangen Sie unternehmensspezifische Ereignisse**

1.  Kompilieren Sie die MIB-Definitionen vom Gerät, das für die Generierung des Ereignisses verantwortlich ist.

    Sie können die MIB-Definitionen mit dem SNMP MIB-Compiler kompilieren. Weitere Informationen finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

2.  Bestimmen Sie, welche Klassentypen den Ereignissen zugeordnet werden sollen.

    Wenn Sie die MIB-Definition für ein unternehmensspezifisches Ereignis kompilieren, können Sie bestimmen, welche Art von Klasse der Compiler generiert. Insbesondere können Sie den Compiler anweisen, eine der folgenden Optionen zu erstellen:

    -   [SnmpNotification-Unterklassen](snmpnotification.md) aus den Definitionen.
    -   [SnmpExtendedNotification-Unterklassen](snmpextendednotification.md) aus den Definitionen.
    -   [SnmpNotification-](snmpnotification.md) und [SnmpExtendedNotification-Unterklassen](snmpextendednotification.md) aus den Definitionen.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Wenn die SNMP-Ereignisanbieter einen bestimmten Trap oder eine bestimmte Benachrichtigung empfangen, für die keine Klasse vorhanden ist, generieren die Anbieter ein nicht unternehmensspezifisches Ereignis. Weitere Informationen finden Sie unter [Empfangen von Enterprise nicht spezifischen Ereignissen.](#receiving-enterprise-nonspecific-events)

## <a name="receiving-enterprise-nonspecific-events"></a>Empfangen von Enterprise-Nonspecific Ereignissen

Ein unternehmensfremdes Ereignis ist ein Ereignis, das keiner der Unterklassen von [SnmpNotification](snmpnotification.md) oder [SnmpExtendedNotification](snmpextendednotification.md) oder einer Klasse zugeordnet wird, die ein Unternehmensereignis darstellt.

SEEP verwendet die Klassen **SNMPV1Notification** oder **SNMPV2Notification** für nicht spezifische Ereignisse, während SREP die Klassen **SNMPv1ExtendedNotification** und **SNMPV2ExtendedNotification** verwendet.

Alle vier unternehmensfremden Klassen werden entweder von den Klassen [SnmpNotification](snmpnotification.md) oder [SnmpExtendedNotification](snmpextendednotification.md) abgeleitet und weisen das gleiche Format auf. Beide Klassen verfügen über die einzelne Eigenschaft **VarBindList**. **VarBindList** ist ein Array von Instanzen der **SnmpVarBind-Klasse.** **SnmpVarBind** ist eine Basisklasse, die von den SNMP-Ereignisanbietern unterstützt wird, um eine Instanz einer SNMP-Variablenbindung darzustellen. In der folgenden Tabelle sind die Eigenschaften von **SnmpVarBind** aufgeführt.



| Eigenschaft         | BESCHREIBUNG                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codierung         | Zeichenfolge, die den ASN.1-Typ (Abstract Syntax Notation One) der Variablen in der **Value-Eigenschaft** angibt. |
| ObjectIdentifier | Zeichenfolge, die die Variable in der **Value-Eigenschaft** identifiziert.                                                 |
| Wert            | Rohdaten in Oktetten.                                                                                            |



 

In den Klassen **SnmpV1Notification** und **SnmpV2Notification** wurde die Reihenfolge der Variablenbindung aus dem SNMP-Ereignis beibehalten, mit Ausnahme der ersten beiden Variablenbindungen TimeStamp und SnmpTrapOID. Diese Bindungen wurden entfernt und in den **Eigenschaften TimeStamp** und **Identification** der [übergeordneten Klasse SnmpNotification](snmpnotification.md) oder [SnmpExtendedNotification](snmpextendednotification.md) gespeichert.

 

 



