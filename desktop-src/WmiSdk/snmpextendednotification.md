---
description: Die SnmpExtendedNotification-Klasse ist die Basisklasse für jede Klasse, die vom NOTIFICATION-TYPE-Makro einer CIM-Klasse durch den SNMP-Anbieter zugeordnet wird.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: d8da8533e9ac5c86dfa3291092fb5165b94e2e393e507c55f15b64c1e30cd6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816540"
---
# <a name="snmpextendednotification-class"></a>SnmpExtendedNotification-Klasse

Die **SnmpExtendedNotification-Klasse** ist die Basisklasse für jede Klasse, die vom [NOTIFICATION-TYPE-Makro einer CIM-Klasse](notification-type-macro.md) vom [SNMP-Anbieter zugeordnet wird.](snmp-provider.md)

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
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

Die **SnmpExtendedNotification-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SnmpExtendedNotification-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Netzwerkadresse der Entität, die die Benachrichtigung erstellt hat. Dies ist die tatsächliche Adresse des Geräts. Wenn die Verwaltungsentität SNMP über UDP verwendet, verweist die Transportadresse auf eine IP-Adresse. Wenn die Verwaltungsentität SNMP über IPX verwendet, wird die Transportadresse auf **NULL festgelegt.** Diese Eigenschaft ist nur für SNMPv1 gültig.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Transportprotokoll, das von der sendenden Entität verwendet wird. Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Netzwerkadresse der Entität, die die Benachrichtigung gesendet hat. Dies ist die Adresse der letzten Entität, die die Benachrichtigung weitergeleitet hat. Wenn die Verwaltungsentität SNMP über UDP verwendet, verweist die Transportadresse auf eine IP-Adresse. Wenn die Verwaltungsentität SNMP über IPX verwendet, verweist die Transportadresse auf eine IPX-Adresse. Diese Eigenschaft ist für SNMPv1 und SNMPv2C gültig.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das transport-Protokoll, das von der sendenden Entität verwendet wird.

</dd> <dt>

**Community**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Community name, der einer Instanz des PDU zugeordnet ist. Der Communityname authentifiziert den Erursacher der PDU. Diese Eigenschaft ist sowohl für SNMPv1 als auch für SNMPv2C gültig.

</dd> <dt>

**Identification**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Textkonvention \_** ("OBJECTIDENTIFIER"),  Codierung ("OBJECTIDENTIFIER"), Objektsyntax ("OBJECTIDENTIFIER"), Objektbezeichner ("1.3.6.1.6.3.1.1.4.1") **\_** **\_**
</dt> </dl>

Autoritative Identifikation dieser Benachrichtigung. Karten direkt an die SnmpTrapOID-Variablenbindung des MIB-Eintrags. Diese Eigenschaft ist nur für SNMPv2C gültig.

</dd> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md) Weitere Informationen zu Konstanten, die zum Festlegen dieses Sicherheitsdeskriptors verwendet werden, finden Sie unter [WMI-Sicherheitskonst constants](wmi-security-constants.md).

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Coordinated Universal Times) angegeben. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Textkonvention \_** ("TimeTicks"),  Codierung ("TimeTicks"), Objektsyntax ("TimeTicks"), Objektbezeichner ("1.3.6.1.2.1.1.3") **\_** **\_**
</dt> </dl>

Die Zeit in 1/100 Sekunden, seit der Netzwerkverwaltungsteil des Agents zuletzt neu initialisiert wurde. Dies wird der MIB-Variablen sysUptime.0 vom Typ **INTEGER32 zugewiesen.** Diese Eigenschaft wird der CIM-Klasseneigenschaft **TimeStamp vom** Typ **uint32 zu.** Diese Eigenschaft ist nur für SNMPv2C gültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein [NOTIFICATION-TYPE-Makro,](notification-type-macro.md) das Verweise auf ein [OBJECT-TYPE-Makro](object-type-macro.md) namens **TimeStamp** oder **Identification** enthält, verursacht einen Zuordnungskonflikt. Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.

Ein [NOTIFICATION-TYPE-Makro,](notification-type-macro.md) das Verweise auf ein [OBJECT-TYPE-Makro](object-type-macro.md) namens enthält, **Community** einen Zuordnungskonflikt verursacht. Wenn dieser Konflikt auftritt, haben die erforderlichen Eigenschaften Vorrang, und die in Konflikt stehenden Verweise müssen umbenannt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ snmp \\ SMIR<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE-Makro](notification-type-macro.md)
</dt> </dl>

 

