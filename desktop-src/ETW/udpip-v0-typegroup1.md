---
description: 'UdpIp_V0_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.'
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8061009fcf419bd7b5ab04eda0b056a8ccee1ad3f3b990a0846058599f34fbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813762"
---
# <a name="udpip_v0_typegroup1-class"></a>UdpIp \_ V0 \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für UDP/IP-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a>Member

Die **Klasse UdpIp \_ V0 \_ TypeGroup1** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Klasse UdpIp \_ V0 \_ TypeGroup1** verfügt über diese Eigenschaften.

<dl> <dt>

context
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Prozessbezeichner für das Adressobjekt, das die Anforderung erstellt oder empfangen hat.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5), Extension("IPAddr")
</dt> </dl>

Ziel-IP-Adresse.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6), Extension("Port")
</dt> </dl>

Zielportnummer.

</dd> <dt>

dsize
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7)
</dt> </dl>

Größe des Zielpakets.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Extension("IPAddr")
</dt> </dl>

Quell-IP-Adresse.

</dd> <dt>

Größe
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Größe des Quellpakets.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3), Extension("Port")
</dt> </dl>

Quellportnummer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> </dl>

 

 




