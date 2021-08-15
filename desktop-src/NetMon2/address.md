---
description: Ist veraltet und sollte nicht verwendet werden.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: ADDRESS-Struktur (Netmon.h)
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
ms.openlocfilehash: 899d68cb4d041c032ce17ac82866488dfd443071e5368d4ba87950de66a32ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796532"
---
# <a name="address-structure"></a>ADDRESS-Struktur

Die **ADDRESS-Struktur** ist veraltet und sollte nicht verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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

**Typ**
</dt> <dd>

Adresstyp. Folgende Werte sind möglich:

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Ansicht der Daten, die als unformatte MAC-Adresse ausgedrückt werden.

</dd> <dt>

**IPAddress**
</dt> <dd>

Ansicht der Daten, die als unformatte IP-Adresse ausgedrückt werden.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Ansicht der Daten, die als UN-IPX-Adresse ausgedrückt werden.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Ansicht der Daten, die als decodierten IPX-Adresswert ausgedrückt werden.

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

Ansicht der Daten, die als Unformatierung der Vines-IP-Adresse ausgedrückt werden.

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

Ansicht der Daten, die als decodierte Vines-IP-Adresse ausgedrückt werden.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Ansicht der Daten, die als Ethernet-Quelladresse ausgedrückt werden.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Ansicht der Daten, die als Ethernet-Zieladresse ausgedrückt werden.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Eine Ansicht der Daten als Tokenring-Quelladresse.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Eine Ansicht der Daten als Zieladresse des Tokenrings.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Ansicht der Daten, die als FDDI-Quelladresse ausgedrückt werden.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Ansicht der Daten, die als FDDI-Zieladresse ausgedrückt werden.

</dd> <dt>

**Flags**
</dt> <dd>

Ein Satz von Flags, die die Adresseigenschaften ändern.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




