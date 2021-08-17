---
description: Die QueryId-Methode ruft einen Bezeichner für den Pin ab.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: CSourceStream.QueryId-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd8582d16022c9d5dfd60eb87847d564ef69203e329ff37eaa9c2964a11794c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317510"
---
# <a name="csourcestreamqueryid-method"></a>CSourceStream.QueryId-Methode

Die `QueryId` -Methode ruft einen Bezeichner für den Pin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Zeiger auf eine Variable, die eine Zeichenfolge empfängt, die den Pinbezeichner enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                       | Beschreibung                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Nicht genügend Arbeitsspeicher.<br/>             |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>         |  NULL-Zeigerargument.<br/>       |
| <dl> <dt>**VFW \_ E \_ NICHT \_ GEFUNDEN**</dt> </dl> | Die Stecknadel wurde im Filter nicht gefunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die [**IPin::QueryId-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) Um eine Bezeichnerzeichenfolge zu erstellen, ruft der Pin die [**CSource::FindPinNumber-Methode**](csource-findpinnumber.md) mit sich selbst als Parameter auf. Die **FindPinNumber-Methode** gibt die Pinnummer zurück, indiziert von 0 (null). `QueryId` erhöht den Rückgabewert um 1 und konvertiert das Ergebnis in eine Zeichenfolge. Der erste Pin wird z. B. zu "1". Der zweite Pin wird zu "2"; usw.

Wenn diese Methode VFW E NOT FOUND zurückgibt, gibt sie an, dass das Array von Pins des Filters ungültig ist, was vermutlich durch einen Fehler \_ \_ im Filter verursacht \_ wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




