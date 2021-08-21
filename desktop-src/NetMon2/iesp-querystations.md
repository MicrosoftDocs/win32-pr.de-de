---
description: Die QueryStations-Methode stellt eine Liste aller Computer zur Verfügung, die Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: IESP::QueryStations-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b116ef2ce5191ab1d086fab78fcadb7df55af5f6e170f6e909d6cde96d10e41d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063950"
---
# <a name="iespquerystations-method"></a>IESP::QueryStations-Methode

Die **QueryStations-Methode** stellt eine Liste aller Computer zur Verfügung, die Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.

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

Zeiger auf eine [QUERYTABLE-Struktur.](querytable.md) Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern, die von Netzwerkmonitor werden sollen, und ein Array von [STATIONQUERY-Strukturen](stationquery.md) enthalten.

Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [STATIONQUERY-Struktur](stationquery.md) für jeden gefundenen Computer. Beachten Sie, dass diese Summe Computer umfassen kann, die Versionen von Netzwerkmonitor, die Vorversion 2.0 verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                           | Beschreibung                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Der zum Verarbeiten dieser Abfrage benötigte Arbeitsspeicher war nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann jederzeit aufgerufen werden, nachdem die [CreateNPPInterface-Methode](createnppinterface.md) aufgerufen wurde. Ein Aufruf dieser Methode ist ein synchroner Aufruf, der einige Sekunden dauern kann, da Netzwerkmonitor auf die Antwort der Remotecomputer auf die Abfrage wartet. Nur Computer im lokalen Subnetz können abgefragt werden.

Es liegt in Ihrer Verantwortung, den Arbeitsspeicher für die [QUERYTABLE-Struktur](querytable.md) zu reservieren und diesen Freispeicher frei zu geben, nachdem die Tabelle nicht mehr benötigt wird. Diese Anforderung umfasst den Arbeitsspeicher, der für das [in QUERYTABLE verwendete STATIONQUERY-Array](stationquery.md) benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[Querytable](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




