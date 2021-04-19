---
description: Enthält eine einzelne Adresse eines beliebigen Typs unterstützter Adressen.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: ADDRESS2-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356139"
---
# <a name="address2-structure"></a>ADDRESS2-Struktur

Die **Adress** Struktur enthält eine einzelne Adresse eines beliebigen Typs unterstützter Adressen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Adresstyp. Folgende Werte sind möglich:

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IP6</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Anzeigen der Daten, die als unformatierte Mac-Adresse ausgedrückt werden.

</dd> <dt>

**IPAddress**
</dt> <dd>

Sicht der Daten, die als unformatierte IP-Adresse ausgedrückt werden.

</dd> <dt>

**IP6Address**
</dt> <dd>

Anzeigen der Daten, die als Rohdaten der IP-Version 6 ausgedrückt werden.

</dd> <dt>

**Ipxrawaddress**
</dt> <dd>

Sicht der Daten, die als unformatierte IPX-Adresse ausgedrückt werden.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Sicht der Daten, die als decodierte IPX-Adress Werte ausgedrückt werden.

</dd> <dt>

**Vinesiprawaddress**
</dt> <dd>

Anzeigen der Daten, die als Rohdaten für die Reben-IP-Adresse ausgedrückt werden.

</dd> <dt>

**Vinesipaddress**
</dt> <dd>

Ansicht der Daten, die als decodierte IP-Adresse für die Reben ausgedrückt werden.

</dd> <dt>

**Ethernetzrcaddress**
</dt> <dd>

Sicht der Daten, die als Ethernet-Quelladresse ausgedrückt werden.

</dd> <dt>

**Ethernetdstaddress**
</dt> <dd>

Sicht der Daten, die als Ethernet-Zieladresse ausgedrückt werden.

</dd> <dt>

**"Dekenringsrcaddress"**
</dt> <dd>

Eine Ansicht der Daten als Quelladresse für den Tokenring.

</dd> <dt>

**Verzeichnis-dstaddress**
</dt> <dd>

Eine Ansicht der Daten als Zieladresse für den Tokenring.

</dd> <dt>

**"Rddisrcaddress"**
</dt> <dd>

Sicht der Daten, die als eine "f"-Quelladresse ausgedrückt werden.

</dd> <dt>

**"F"**
</dt> <dd>

Die Ansicht der Daten, die als eine Adresse für ein BDI-Ziel ausgedrückt werden.

</dd> <dt>

**Flags**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




