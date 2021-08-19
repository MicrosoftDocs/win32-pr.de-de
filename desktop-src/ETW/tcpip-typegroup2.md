---
description: Diese Klasse ist die Ereignistypklasse für IPv4-TCP/IP-Verbindungs- und Accept-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 316daec5b6bb186756f8597a63ee35d18125181b6575ae24c8ba8fae63f53d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814500"
---
# <a name="tcpip_typegroup2-class"></a>TcpIp \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistypklasse für IPv4-TCP/IP-Verbindungs- und Accept-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Member

Die **TcpIp \_ TypeGroup2-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **TcpIp \_ TypeGroup2-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**connid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(15)**, **Zeiger**
</dt> </dl>

Ein eindeutiger Verbindungsbezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.

</dd> <dt>

**daddr**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(3)**, **Extension("IPAddrV4")**
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(5)**, **Extension("Port")**
</dt> </dl>

Zielportnummer.

</dd> <dt>

**Mss**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(7)**
</dt> </dl>

Maximale Segmentgröße.

</dd> <dt>

**Pid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(1)**
</dt> </dl>

Bezeichner des Prozesses, der der Anforderung zugeordnet ist.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(11)**
</dt> </dl>

Größe des TCP-Empfangsfensters.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(12)**
</dt> </dl>

Skalierungsfaktor für TCP-Empfangsfenster.

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(8)**
</dt> </dl>

Option "Selektive Bestätigung" (Selective Acknowledgment, TIVE) im TCP-Header.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(4)**, **Extension("IPAddrV4")**
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

**seqnum**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(14)**
</dt> </dl>

Sequenznummer.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(2)**
</dt> </dl>

Größe des Pakets.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(13)**
</dt> </dl>

Skalierungsfaktor für TCP-Sendefenster.

</dd> <dt>

**Sport**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(6)**, **Extension("Port")**
</dt> </dl>

Quellportnummer.

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(9)**
</dt> </dl>

Zeitstempeloption im TCP-Header.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId(10)**
</dt> </dl>

Fensterskalierungsoption im TCP-Header.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




