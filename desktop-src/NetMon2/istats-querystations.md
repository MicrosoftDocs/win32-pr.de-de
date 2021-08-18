---
description: Die QueryStations-Methode stellt eine Liste aller Computer bereit, die derzeit Daten mithilfe Netzwerkmonitor erfassen.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: IStats::QueryStations-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2d4ead22b3e7308aee3c44b3ff6dff407591cbe675b09a3300f3e7a8720726c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742640"
---
# <a name="istatsquerystations-method"></a>IStats::QueryStations-Methode

Die **QueryStations-Methode** stellt eine Liste aller Computer bereit, die derzeit Daten mit Netzwerkmonitor erfassen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpQueryTable* \[ in, out\]
</dt> <dd>

Zeiger auf eine [QUERYTABLE-Struktur.](querytable.md) Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern enthalten, die Netzwerkmonitor zurückgeben möchten, sowie ein Array von [STATIONQUERY-Strukturen.](stationquery.md)

Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [STATIONQUERY-Struktur](stationquery.md) für jeden gefundenen Computer. Beachten Sie, dass diese Informationen Computer enthalten können, die Versionen von Netzwerkmonitor vor Version 2.0 verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                           | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Der zum Verarbeiten dieser Abfrage erforderliche Arbeitsspeicher war nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann jederzeit aufgerufen werden, nachdem [CreateNPPInterface](createnppinterface.md) aufgerufen wurde. Ein Aufruf dieser Methode ist ein synchroner Aufruf, der einige Sekunden dauern kann, da Netzwerkmonitor wartet, bis Remotecomputer auf die Abfrage reagieren. Nur Computer im lokalen Subnetz können abgefragt werden.

Es liegt in Ihrer Verantwortung, den Arbeitsspeicher für die [QUERYTABLE-Struktur](querytable.md) zuzuordnen und diesen Arbeitsspeicher freizugeben, nachdem die Tabelle nicht mehr benötigt wird. Diese Anforderung umfasst den Arbeitsspeicher, der für das in QUERYTABLE verwendete [STATIONQUERY-Array](stationquery.md) benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[Querytable](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




