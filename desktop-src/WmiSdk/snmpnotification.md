---
description: Die SnmpNotification-Klasse wird aus dem Notification-Type-Makro einer gekapselten CIM-Klasse zugeordnet.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: SnmpNotification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530209"
---
# <a name="snmpnotification-class"></a>SnmpNotification-Klasse

Die **SnmpNotification** -Klasse wird aus dem [Notification-Type-](notification-type-macro.md) Makro einer gekapselten CIM-Klasse zugeordnet. Dabei handelt es sich um eine Basisklasse, die vom [SNMP-Anbieter](snmp-provider.md) für jede Klasse verwendet wird, die vom [Notification-Type-](notification-type-macro.md) Makro einer gekapselten CIM-Klasse des SNMP-Anbieters zugeordnet wird.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

## <a name="syntax"></a>Syntax

``` syntax
class SnmpNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a>Member

Die **SnmpNotification** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SnmpNotification** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Netzwerkadresse der Entität, die die Benachrichtigung erstellt hat. Dies ist die tatsächliche Adresse des Geräts. Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse. Wenn die Verwaltungs Entität SNMP über IPX verwendet, wird die Transport Adresse auf **null** festgelegt. Diese Eigenschaft ist nur für SNMPv1 gültig.

</dd> <dt>

**Agenttransport**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Von der sendenden Entität verwendetes Transport Protokoll. Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.

</dd> <dt>

**Agenttransportaddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Netzwerkadresse der Entität, die die Benachrichtigung gesendet hat. Dies ist die Adresse der letzten Entität, die die Benachrichtigung weitergeleitet hat. Wenn die Verwaltungs Entität SNMP über UDP verwendet, bezieht sich die Transport Adresse auf eine IP-Adresse. Wenn die Verwaltungs Entität SNMP über IPX verwendet, bezieht sich die Transport Adresse auf eine IPX-Adresse. Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.

</dd> <dt>

**Agenttransportprotocol**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Transportprotokoll, das von der sendenden Entität verwendet wird.

</dd> <dt>

**Community**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Communityname, der einer Instanz des PDU zugeordnet ist. Der Communityname authentifiziert den Absender des PDU. Diese Eigenschaft ist sowohl für SNMPv1 als auch für SNMPv2C gültig.

</dd> <dt>

**Identifikation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Text \_ Konvention** ("objectidentifier"), **Codierung** ("objectidentifier"), **Objekt \_ Syntax** ("objectidentifier"), **Objekt \_ Bezeichner** ("1.3.6.1.6.3.1.1.4.1")
</dt> </dl>

Autorisierende Identifizierung dieser Benachrichtigung. Wird direkt der snmptrapoid-Variablen Bindung zugeordnet. Diese Eigenschaft ist nur für SNMPv2C gültig.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt. Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Zeitstempel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Text \_ Konvention** ("TimeTicks"), **Codierung** ("TimeTicks"), **Objekt \_ Syntax** ("TimeTicks"), **Objekt \_ Bezeichner** ("1.3.6.1.2.1.1.3")
</dt> </dl>

Zeit in Hundertstel Sekunden, seit der Netzwerk Verwaltungsteil des Agents zuletzt erneut initialisiert wurde. MIB-Variable "sysUpTime. 0", die vom Typ " **INTEGER32**" ist. Diese Eigenschaft wird der Eigenschaft **timestamp** der CIM-Klasse zugeordnet, die vom Typ **UInt32** ist. Diese Eigenschaft ist nur für SNMPv2C gültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein [Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp](object-type-macro.md) Makro mit dem Namen **timestamp** oder **Identification** enthält, verursacht einen Mapping-Konflikt. Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.

Ein [-Benachrichtigungstyp](notification-type-macro.md) Makro, das Verweise auf ein [Objekttyp-](object-type-macro.md) Makro namens **Community** enthält, verursacht einen zuordnungskonflikt. Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>   |
| Namespace<br/>                | Root \\ SNMP- \\ localhost<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Notification-Type-Makro](notification-type-macro.md)
</dt> </dl>

 

