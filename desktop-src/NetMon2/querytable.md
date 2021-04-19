---
description: Die QueryTable-Struktur enthält eine Liste der Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: QueryTable-Struktur (Netmon. h)
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
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347954"
---
# <a name="querytable-structure"></a>QueryTable-Struktur

Die **QueryTable** -Struktur enthält eine Liste der Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**nstationqueries**
</dt> <dd>

Bei Eingabe die maximale Anzahl von Computern, die Netzwerkmonitor zurückgegeben werden soll.

Bei Ausgabe die Anzahl der [stationquery](stationquery.md) -Strukturen, die von Netzwerkmonitor zurückgegeben werden. Jede **stationquery** -Struktur stellt einen Computer dar, der zurzeit Daten erfasst.

</dd> <dt>

**Stationquery**
</dt> <dd>

Bei Eingabe ein Array leerer [stationquery](stationquery.md) -Strukturen, das die Anzahl der in **nstationqueries** angegebenen Elemente enthält.

Bei Ausgabe eine gefüllte [Stations Abfrage](stationquery.md) Struktur für jeden Computer, der Daten erfasst. Die Anzahl der gefüllten Elemente wird von **nstationqueries** zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Arbeitsspeicher für diese Struktur und das [stationquery](stationquery.md) -Array müssen von der aufrufenden Anwendung zugeordnet und freigegeben werden, nachdem die Informationen nicht mehr benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC:: querystations](idelaydc-querystations.md)
</dt> <dt>

[IESP:: querystations](iesp-querystations.md)
</dt> <dt>

["Iran:: querystations"](irtc-querystations.md)
</dt> <dt>

[IStats:: querystations](istats-querystations.md)
</dt> <dt>

[Stationquery](stationquery.md)
</dt> </dl>

 

 




