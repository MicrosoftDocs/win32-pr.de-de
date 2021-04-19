---
description: Die querystations-Methode enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'IESP:: querystations-Methode (Netmon. h)'
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
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346073"
---
# <a name="iespquerystations-method"></a>IESP:: querystations-Methode

Die **querystations** -Methode enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.

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

Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [stationquery](stationquery.md) -Struktur für jeden gefundenen Computer. Beachten Sie, dass diese Summe Computer enthalten kann, die Versionen von Netzwerkmonitor, für die die Version 2,0 in der Vorschauversion

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                           | Beschreibung                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl> | Der für die Verarbeitung dieser Abfrage erforderliche Arbeitsspeicher war nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [comatenppinterface](createnppinterface.md) " aufgerufen wurde. Ein Rückruf für diese Methode ist ein synchroner Vorgang, der einige Sekunden in Anspruch nehmen kann, da Netzwerkmonitor darauf wartet, dass Remote Computer auf die Abfrage antworten. Nur Computer im lokalen Subnetz können abgefragt werden.

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

[IESP](iesp.md)
</dt> <dt>

[QueryTable](querytable.md)
</dt> <dt>

[Stationquery](stationquery.md)
</dt> </dl>

 

 




