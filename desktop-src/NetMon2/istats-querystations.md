---
description: Die querystations-Methode enthält eine Liste aller Computer, die derzeit Daten mit Netzwerkmonitor erfassen.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: 'IStats:: querystations-Methode (Netmon. h)'
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
ms.openlocfilehash: 99c3be3926191c27ad038034373e411b5c22d9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042700"
---
# <a name="istatsquerystations-method"></a>IStats:: querystations-Methode

Die **querystations** -Methode enthält eine Liste aller Computer, die derzeit Daten mit Netzwerkmonitor erfassen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpquerytable* \[ in, out\]
</dt> <dd>

Zeiger auf eine [QueryTable](querytable.md) -Struktur. Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern enthalten, die Netzwerkmonitor zurückgegeben werden sollen, sowie ein Array von [stationquery](stationquery.md) -Strukturen.

Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [stationquery](stationquery.md) -Struktur für jeden gefundenen Computer. Beachten Sie, dass diese Informationen möglicherweise Computer enthalten, die Versionen von Netzwerkmonitor, die der Version 2,0 vorausgehen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                           | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl> | Der für die Verarbeitung dieser Abfrage erforderliche Arbeitsspeicher war nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem " [comatenppinterface](createnppinterface.md) " aufgerufen wurde. Ein Rückruf für diese Methode ist ein synchroner Vorgang, der einige Sekunden in Anspruch nehmen kann, da Netzwerkmonitor darauf wartet, dass Remote Computer auf die Abfrage antworten. Nur Computer im lokalen Subnetz können abgefragt werden.

Es liegt in ihrer Verantwortung, den Arbeitsspeicher für die [QueryTable](querytable.md) -Struktur zuzuordnen und diesen Arbeitsspeicher freizugeben, nachdem die Tabelle nicht mehr benötigt wird. Diese Anforderung enthält den Arbeitsspeicher, der für das in QueryTable verwendete [stationquery](stationquery.md) -Array benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[QueryTable](querytable.md)
</dt> <dt>

[Stationquery](stationquery.md)
</dt> </dl>

 

 




