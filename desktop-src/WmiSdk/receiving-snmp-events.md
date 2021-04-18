---
description: Die SNMP-Ereignis Anbieter unterstützen SNMPv1 Traps und SNMPv2-Benachrichtigungen.
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: Empfangen von SNMP-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348125"
---
# <a name="receiving-snmp-events"></a>Empfangen von SNMP-Ereignissen

Die SNMP-Ereignis Anbieter unterstützen SNMPv1 Traps und SNMPv2-Benachrichtigungen.

Die folgenden drei Arten von SNMPv1 Traps und SNMPv2-Benachrichtigungen werden unterstützt:

-   Allgemein

    Generische Traps und Benachrichtigungen entsprechen benannten Ereignissen wie z. b. Link Up und Kaltstart. Generische Traps und Benachrichtigungen werden durch Klassen dargestellt, wie z. b. **snmplinkupnotification** und **snmpwarmstartextendednotification**, die den Namen des Traps im Klassennamen enthalten. Diese Klassen sind Unterklassen von [SnmpNotification](snmpnotification.md) und [snmpextendednotification](snmpextendednotification.md).

-   Unternehmensspezifisch

    Unternehmensspezifische Traps und Benachrichtigungen entsprechen Ereignissen, die durch eine WMI-Klasse dargestellt werden, die keine Unterklasse von " [SnmpNotification](snmpnotification.md) " und " [snmpextendednotification](snmpextendednotification.md)" ist. Zur Unterstützung von unternehmensspezifischen Traps und Benachrichtigungen muss ein Consumer Klassen definieren, indem MIB-Definitionen mithilfe des SNMP-MIB-Compilers kompiliert werden.

-   Enterprise-nonspecific

    Nicht Enterprise-spezifische Traps und Benachrichtigungen entsprechen keinem der generischen Ereignis Typen oder unternehmensspezifischen Ereignis Typen. Bei nicht unternehmensspezifischen Traps und Benachrichtigungen wurden ihre MIB-Definitionen nicht in SMIR kompiliert. Sie werden durch die Klassen [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification** und **SnmpV2ExtendedNotification** dargestellt, die von SnmpNotification und [snmpextendednotification](snmpextendednotification.md)abgeleitet werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Empfangen von generischen SNMP-Ereignissen](#receiving-generic-snmp-events)
-   [Empfangen von Enterprise-Specific Ereignissen](#receiving-enterprise-specific-events)
-   [Empfangen von Enterprise-Nonspecific Ereignissen](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a>Empfangen von generischen SNMP-Ereignissen

Die Datentypen "abkep" und "SREP" unterstützen alle Typen allgemeiner SNMPv1 Traps und SNMPv2-Benachrichtigungen Generische SNMP-Ereignisse werden durch Unterklassen der Klassen " [SnmpNotification](snmpnotification.md) " und " [snmpextendednotification](snmpextendednotification.md) " dargestellt.

Jeder Ereignistyp wird durch eine Klasse "-Klasse" und eine SREP-Klasse dargestellt. Die abgeleiteten Klassen werden von [SnmpNotification](snmpnotification.md)abgeleitet. die SREP-Klassen werden von [snmpextendednotification](snmpextendednotification.md)abgeleitet. Die Ereignis Anbieter benötigen unterschiedliche Klassen, da Sie unterschiedliche Mechanismen in der Darstellung der SNMP-Ereignisdaten verwenden.

Das DataSet konvertiert die SNMP-Ereignisdaten direkt in WMI-Klasseneigenschaften, wohingegen die SREP nicht. Der SREP fügt der Interpretation, die für die Verwendung der WMI-Eigenschaften erforderlich ist, eine Dereferenzierungsebene hinzu. Die Eigenschaften der SREP- [snmpextendednotification](snmpextendednotification.md) -Unterklassen sind Instanzen von SNMP-Klassen. die Eigenschaften der Seep- [SnmpNotification](snmpnotification.md) -Unterklassen sind ganze Zahlen und Zeichen folgen.

In der folgenden Tabelle sind die Typen von generischen SNMP-Ereignissen und die zugehörigen Ereignis Klassen aufgeführt.



| SNMP-Ereignis                                    | Klasse "Klasse"                                | SREP-Klasse                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| Authentifizierungsfehler                        | **Snmpauthenticationfailurenotifizierung** | **Snmpauthenticationfailureextendednotification** |
| EGP-Nachbar Verlust (outside Gateway Protocol) | **Snmpegpnachbarlossnotification**       | **Snmpegpnachbarlossextendednotification**       |
| Kaltstart                                    | **Snmpcoldstartnotification**             | **Snmpcoldstartextendednotification**             |
| Warmstart                                    | **Snmpwarmstartnotification**             | **Snmpwarmstartextendednotification**             |
| Verknüpfung einrichten                                       | **Snmplinkupnotification**                | **Snmplinkupextendednotification**                |
| Link nach unten                                     | **Snmplinkdownnotification**              | **Snmplinkdownextendednotification**              |



 

Die Klassen **snmplinkupnotification** und **snmplinkupextendednotification** beschreiben z. b. das Verknüpfungs Ereignis. Beide Klassen enthalten die Eigenschaften " **ifindex**", " **ifadminstatus**" und " **ifOperStatus** ", aber Sie verfügen über sehr unterschiedliche Typen. Die Eigenschaften in der **snmplinkupnotification** -Klasse sind vom Typ SINT32 und String. Die Eigenschaften in der **snmplinkupextendednotification** -Klasse sind der eingebettete Objekttyp IETF \_ SNMP \_ RFC1213 \_ MIB \_ iftable.

## <a name="receiving-enterprise-specific-events"></a>Empfangen von Enterprise-Specific Ereignissen

Seep und SREP unterstützen alle unternehmensspezifischen Traps und Benachrichtigungen, die Sie in SMIR kompiliert haben.

Im folgenden Verfahren wird beschrieben, wie Sie unternehmensspezifische Ereignisse empfangen.

**So empfangen Sie unternehmensspezifische Ereignisse**

1.  Kompilieren Sie die MIB-Definitionen von dem Gerät, das für das Erstellen des Ereignisses verantwortlich ist.

    Die MIB-Definitionen können mithilfe des SNMP-MIB-Compilers kompiliert werden. Weitere Informationen finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

2.  Bestimmen Sie, welche Typen von Klassen Sie den Ereignissen zuordnen möchten.

    Wenn Sie die MIB-Definition für ein unternehmensspezifisches Ereignis kompilieren, können Sie bestimmen, welche Art von Klasse der Compiler generiert. Insbesondere können Sie den Compiler anweisen, eine der folgenden Optionen zu erstellen:

    -   [SnmpNotification](snmpnotification.md) -Unterklassen aus den Definitionen.
    -   [Snmpextendednotification](snmpextendednotification.md) -Unterklassen aus den-Definitionen.
    -   Die Unterklassen " [SnmpNotification](snmpnotification.md) " und " [snmpextendednotification](snmpextendednotification.md) " aus den Definitionen.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Wenn die SNMP-Ereignis Anbieter einen bestimmten Trap oder eine Benachrichtigung erhalten, für die keine Klasse vorhanden ist, generieren die Anbieter ein nicht unternehmensspezifisches Ereignis. Weitere Informationen finden Sie [unter empfangen von nicht spezifischen Enterprise-Ereignissen](#receiving-enterprise-nonspecific-events).

## <a name="receiving-enterprise-nonspecific-events"></a>Empfangen von Enterprise-Nonspecific Ereignissen

Ein nicht bestimmtes Enterprise-Ereignis ist ein Ereignis, das nicht von einer SNMPv1 Trap-oder SNMPv2-Benachrichtigung zu einer der Unterklassen von [SnmpNotification](snmpnotification.md) oder [snmpextendednotification](snmpextendednotification.md) oder einer Klasse, die ein Enterprise-Ereignis darstellt, zugeordnet wird.

Die Klassen " **SNMPV1Notification** " und " **SNMPV2Notification** " werden für nicht spezifische Ereignisse verwendet, wohingegen "SREP" die Klassen **SNMPv1ExtendedNotification** und **SNMPV2ExtendedNotification** verwendet.

Alle vier Enterprise-nicht spezifischen Klassen werden entweder von der [SnmpNotification](snmpnotification.md) -Klasse oder von der [snmpextendednotification](snmpextendednotification.md) -Klasse abgeleitet und weisen das gleiche Format auf. Beide Klassen verfügen über die einzelne **varbindlist**-Eigenschaft. **Varbindlist** ist ein Array von Instanzen der **snmpvarbind** -Klasse. **Snmpvarbind** ist eine Basisklasse, die von den SNMP-Ereignis Anbietern unterstützt wird, um eine Instanz einer SNMP-Variablen Bindung darzustellen. In der folgenden Tabelle sind die Eigenschaften von **snmpvarbind** aufgeführt.



| Eigenschaft         | BESCHREIBUNG                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| Codierung         | Eine Zeichenfolge, die den Typ der abstrakten Syntax Notation One (ASN. 1) der Variablen in der **value** -Eigenschaft angibt. |
| ObjectIdentifier | Eine Zeichenfolge, die die Variable in der **value** -Eigenschaft identifiziert.                                                 |
| Wert            | Rohdaten in Oktette.                                                                                            |



 

In den **SnmpV1Notification** -und **SnmpV2Notification** -Klassen wurde die Variablen Bindungs Reihenfolge des SNMP-Ereignisses mit Ausnahme der ersten beiden Variablen Bindungen (Timestamp und snmptrapoid) beibehalten. Diese Bindungen wurden entfernt und in den **timestamp** -und **Identifizierungs** Eigenschaften der übergeordneten [SnmpNotification](snmpnotification.md) -oder [snmpextendednotification](snmpextendednotification.md) -Klasse gespeichert.

 

 



