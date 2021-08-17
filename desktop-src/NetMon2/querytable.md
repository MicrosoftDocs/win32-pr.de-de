---
description: Die QUERYTABLE-Struktur stellt eine Liste der Computer zur Verfügung, die derzeit Netzwerkmonitor, um Netzwerkdaten zu erfassen.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: QUERYTABLE-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 9b8f291f055bfba159309b6c75a54d95514ed9c7614eb0456a4870e657f04209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555370"
---
# <a name="querytable-structure"></a>QUERYTABLE-Struktur

Die **QUERYTABLE-Struktur** stellt eine Liste der Computer zur Verfügung, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**nStationQueries**
</dt> <dd>

Bei der Eingabe die maximale Anzahl von Computern, die von Netzwerkmonitor werden soll.

Bei der Ausgabe wird die Anzahl der [stationquery-Strukturen,](stationquery.md) die von zurückgegeben werden, Netzwerkmonitor. Jede **STATIONQUERY-Struktur** stellt einen Computer dar, der derzeit Daten erfasst.

</dd> <dt>

**StationQuery**
</dt> <dd>

Bei der Eingabe ein Array leerer [STATIONQUERY-Strukturen,](stationquery.md) das die Anzahl der in **nStationQueries angegebenen Elemente enthält.**

Bei der Ausgabe eine gefüllte [STATIONQUERY-Struktur](stationquery.md) für jeden Computer, der Daten erfasst. Die Anzahl der ausgefüllten Elemente wird von **nStationQueries zurückgegeben.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Arbeitsspeicher für diese Struktur und das [STATIONQUERY-Array](stationquery.md) muss von der aufrufenden Anwendung zugeordnet und wieder frei werden, nachdem die Informationen nicht mehr benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




