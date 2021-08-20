---
description: 'UdpIp_Fail Klasse: Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: UdpIp_Fail-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3cb58c7262e46dde761d1494bc26b5a5701489f7e5aed167e1edf85bd9789f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813802"
---
# <a name="udpip_fail-class"></a>UdpIp \_ Fail-Klasse

Diese Klasse ist die Ereignistypklasse für TCP/IP-Fehlerereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Member

Die **UdpIp \_ Fail-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **UdpIp \_ Fail-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FailureCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Ursache für den Fehler. Kann einer der folgenden Codes sein:

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**FEHLER \_ UNZUREICHENDE \_ RESSOURCEN** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**FEHLER \_ ZU \_ VIELE \_ ADRESSEN** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**FEHLER \_ ADDRESS \_ EXISTS** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**FEHLER \_ UNGÜLTIGE \_ ADRESSE** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**FEHLER \_ OTHER** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**FEHLER \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert das Protokoll. Es kann sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                                                  | Bedeutung                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | Die Internetprotokoll, Version 4 -Adressfamilie (IPv4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | Die IPv6-Adressfamilie (Internet Protocol Version 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




