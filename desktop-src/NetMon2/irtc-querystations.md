---
description: Enthält eine Liste aller Computer, die derzeit Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Untc:: querystations-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959385"
---
# <a name="irtcquerystations-method"></a>"Iritc:: querystations"-Methode

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

Ein Zeiger auf eine [**QueryTable**](querytable.md) -Struktur. Bei der Eingabe muss diese Struktur die maximale Anzahl von Computern enthalten, die Netzwerkmonitor zurückgegeben werden sollen, sowie ein Array von [**stationquery**](stationquery.md) -Strukturen.

Bei der Ausgabe gibt diese Struktur die Anzahl der Computer zurück, die Daten erfassen, und eine [**stationquery**](stationquery.md) -Struktur für jeden gefundenen Computer. Beachten Sie, dass dies möglicherweise Computer mit Versionen von Netzwerkmonitor ist, die das prädate Version 2,0 aufweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert **nmerr \_ Success**.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl> | Der für die Verarbeitung dieser Abfrage erforderliche Arbeitsspeicher ist nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [**comatenppinterface**](createnppinterface.md) " aufgerufen wurde. Ein Rückruf für diese Methode ist ein synchroner Vorgang, der einige Sekunden in Anspruch nehmen kann, während Netzwerkmonitor darauf wartet, dass Remote Computer auf die Abfrage antworten. Nur Computer im lokalen Subnetz können abgefragt werden.

Der Benutzer muss den Speicher für die [**QueryTable**](querytable.md) -Struktur zuordnen und diesen Arbeitsspeicher freigeben, nachdem die Tabelle nicht mehr benötigt wird. Diese Anforderung umfasst den Arbeitsspeicher, der für das in **QueryTable** verwendete [**stationquery**](stationquery.md) -Array benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Iran"**](irtc.md)
</dt> <dt>

[**QueryTable**](querytable.md)
</dt> <dt>

[**Stationquery**](stationquery.md)
</dt> </dl>

 

 




