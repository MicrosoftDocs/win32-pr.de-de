---
description: Die sessionstats-Struktur enthält Statistiken zu einer Sitzung.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Sessionstats-Struktur (Netmon. h)
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
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215469"
---
# <a name="sessionstats-structure"></a>Sessionstats-Struktur

Die **sessionstats** -Struktur enthält Statistiken zu einer [*Sitzung*](s.md).

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

**Nexzession**
</dt> <dd>

Index der nächsten Sitzung des Stations Besitzers.

</dd> <dt>

**Stationowner**
</dt> <dd>

Index einer Besitzer Station innerhalb des zugeordneten [Stations Statistik](stationstats.md) -Struktur Arrays. Die Besitzer Station ist die Station, die die Sitzung initiiert hat, der Station, die die Pakete der Sitzung gesendet hat.

</dd> <dt>

**Stationpartner**
</dt> <dd>

Index der anderen Station innerhalb des zugeordneten [Stations Statistik](stationstats.md) -Struktur Arrays. Die Partnerstation ist die Station, die die Pakete der Sitzung empfangen hat.

</dd> <dt>

**Flags**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Totalpacketssent**
</dt> <dd>

Anzahl der in der Sitzung gesendeten Pakete.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor speichert Sitzungs-und Stations Informationen in zwei zugeordneten Arrays, deren Elemente **sessionstats** bzw. [stationstats](stationstats.md) -Strukturen sind. Die Member dieser Strukturen können verwendet werden, um zwischen Ihnen zu navigieren. Wenn Sie z. b. zur nächsten Sitzung für einen bestimmten Stations Besitzer wechseln möchten, verwenden Sie **nexzession**. Um zum Besitzer und zur Partnerstation der Sitzung im stationstats-Array zu springen, verwenden Sie den in **stationowner** und **stationpartner** bereitgestellten Index.

> [!Note]  
> Das sessionstats-Array enthält ein-Element für jede Sitzung in der aktuellen Erfassung. Der Netzwerkmonitor Algorithmus, der zum Hinzufügen von Elementen zum sessionstats-Array verwendet wird, basiert auf der effizienten Aufzeichnung von Informationen, während die Erfassung ausgeführt wird. Folglich ist die nächste Sitzung für eine bestimmte Besitzer Station nicht immer das nächste Element im Array.

 

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

 

 




