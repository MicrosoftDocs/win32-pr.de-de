---
description: Die SESSIONSTATS-Struktur stellt Statistiken zu einer Sitzung bereit.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: SESSIONSTATS-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 231c94d2abda40974249f6c3cc82c8efc7518cb21d5881f44e63f647bcb21de2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128830"
---
# <a name="sessionstats-structure"></a>SESSIONSTATS-Struktur

Die **SESSIONSTATS-Struktur** stellt Statistiken zu einer [*Sitzung*](s.md)bereit.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**NextSession**
</dt> <dd>

Index der nächsten Sitzung des Stationsbesitzers.

</dd> <dt>

**StationOwner**
</dt> <dd>

Index einer Besitzerstation innerhalb [](stationstats.md) des zugeordneten STATIONSTATS-Strukturarrays. Die Besitzerstation ist die Station, die die Sitzung initiiert hat, die Station, die die Pakete der Sitzung gesendet hat.

</dd> <dt>

**StationPartner**
</dt> <dd>

Index der anderen Station innerhalb des zugeordneten [STATIONSTATS-Strukturarrays.](stationstats.md) Die Partnerstation ist die Station, die die Pakete der Sitzung empfangen hat.

</dd> <dt>

**Flags**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

Anzahl der in der Sitzung gesendeten Pakete.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Netzwerkmonitor speichert Sitzungs- und Stationsinformationen in zwei zugeordneten Arrays, deren Elemente **SESSIONSTATS-** bzw. [STATIONSTATS-Strukturen](stationstats.md) sind. Die Member dieser Strukturen können verwendet werden, um zwischen ihnen zu navigieren. Um beispielsweise zur nächsten Sitzung für einen bestimmten Stationsbesitzer zu wechseln, verwenden Sie **NextSession**. Um zur Besitzer- und Partnerstation der Sitzung im STATIONSTATS-Array zu wechseln, verwenden Sie den Index, der in **StationOwner** und **StationPartner** bereitgestellt wird.

> [!Note]  
> Das SESSIONSTATS-Array enthält ein Element für jede Sitzung in der aktuellen Erfassung. Der Algorithmus Netzwerkmonitor zum Hinzufügen von Elementen zum SESSIONSTATS-Array verwendet, basiert auf der effizienten Aufzeichnung von Informationen, während die Erfassung ausgeführt wird. Folglich ist die nächste Sitzung für eine bestimmte Besitzerstation nicht immer das nächste Element im Array.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




