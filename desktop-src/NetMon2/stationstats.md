---
description: Die stationstats-Struktur enthält Statistiken zu einer bestimmten Station, die von der aktuellen Erfassung beschrieben wird.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Stationstats-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042070"
---
# <a name="stationstats-structure"></a>Stationstats-Struktur

Die **stationstats** -Struktur enthält Statistiken zu einer bestimmten [*Station*](s.md) , die von der aktuellen Erfassung beschrieben wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**Nextstationstats**
</dt> <dd>

Index der nächsten Station, die im **stationstats** -Struktur Array aufgezeichnet wird.

</dd> <dt>

**Sessionpartnerlist**
</dt> <dd>

Index der Stations Partnerliste.

</dd> <dt>

**Flags**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Stationaddress**
</dt> <dd>

Die Mac-Adresse der Station.

</dd> <dt>

**Pad**
</dt> <dd>

**DWORD** -Ausrichtung.

</dd> <dt>

**Totalpacket empfangen**
</dt> <dd>

Gesamtanzahl der an die Station gesendeten Pakete.

</dd> <dt>

**Totaldirectedpacketssent**
</dt> <dd>

Die Gesamtanzahl der von der Station gesendeten gerichteten Pakete.

</dd> <dt>

**Totalbroadcastpacketssent**
</dt> <dd>

Die Gesamtanzahl der Broadcast gesteuerten Pakete (Mac-Adresse FF FF FF FF FF FF), die von der Station gesendet werden.

</dd> <dt>

**Totalmulticastpacketssent**
</dt> <dd>

Die Gesamtanzahl der Multicast Pakete (in der Zieladresse festgelegtes Gruppen Bit), die von der Station gesendet werden.

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

Gesamtanzahl der an die Station gesendeten Bytes.

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

Die Gesamtanzahl der von der Station gesendeten Bytes.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor speichert Sitzungs-und Stations Informationen in zwei zugeordneten Arrays. , dessen Elemente [sessionstats](sessionstats.md) bzw. **stationstats** -Strukturen sind. Die Member dieser Strukturen können verwendet werden, um zwischen Ihnen zu navigieren. Verwenden Sie beispielsweise **nextstationstats**, um zur nächsten Station zu wechseln. Um zur Sitzungspartner Liste im sessionstats-Array zu springen, verwenden Sie den in **sessionpartnerlist** angegebenen Index.

> [!Note]  
> Das **stationstats** -Array enthält ein-Element für jede Station, die während der aktuellen Erfassung verwendet wird. Der Netzwerkmonitor Algorithmus, der zum Hinzufügen von Elementen zu diesem Array verwendet wird, basiert auf der effizientesten Methode, Informationen aufzuzeichnen, während die Erfassung ausgeführt wird. Folglich ist die nächste Station nicht immer das nächste Element im Array.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta aydc:: getconversation ationstatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

["Irren:: getconversation ationstatistics"](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats:: getconversation ationstatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




