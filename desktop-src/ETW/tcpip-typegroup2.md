---
description: Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP Connect-und Accept-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528220"
---
# <a name="tcpip_typegroup2-class"></a>Tcpip \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistyp Klasse für IPv4-TCP/IP Connect-und Accept-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **tcpip- \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **tcpip- \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**nicht konform**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (15)**, **Zeiger**
</dt> </dl>

Ein eindeutiger Verbindungs Bezeichner zum Korrelieren von Ereignissen, die zur gleichen Verbindung gehören.

</dd> <dt>

**daddr**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (3)**, **Extension ("IPAddrV4")**
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (5)**, **Erweiterung ("Port")**
</dt> </dl>

Die Ziel Portnummer.

</dd> <dt>

**MSS**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (7)**
</dt> </dl>

Maximale Segmentgröße.

</dd> <dt>

**Lauer**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (1)**
</dt> </dl>

Der Bezeichner des Prozesses, der der Anforderung zugeordnet ist.

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (11)**
</dt> </dl>

TCP-Empfangs Fenstergröße.

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (12)**
</dt> </dl>

Skalierungsfaktor für TCP-Empfangs Fenster.

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (8)**
</dt> </dl>

Die Option für die selektive Bestätigung (ACK) im TCP-Header.

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (4)**, **Extension ("IPAddrV4")**
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

**SEQNUM**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (14)**
</dt> </dl>

Sequenznummer.

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (2)**
</dt> </dl>

Größe des Pakets.

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

Datentyp: **sint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (13)**
</dt> </dl>

Skalierungsfaktor für TCP-Sendefenster.

</dd> <dt>

**Reit**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (6)**, **Erweiterung ("Port")**
</dt> </dl>

Quell Portnummer.

</dd> <dt>

**nach-oben**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (9)**
</dt> </dl>

Zeitstempel Option im TCP-Header.

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid (10)**
</dt> </dl>

Fenster Skalierungs Option im TCP-Header.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TcpIp**](tcpip.md)
</dt> </dl>

 

 




