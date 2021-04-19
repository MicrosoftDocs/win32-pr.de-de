---
description: Die QueryId-Methode ruft einen Bezeichner für die PIN ab.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Csourcestream. QueryId-Methode (Quelle. h)
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
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373890"
---
# <a name="csourcestreamqueryid-method"></a>Csourcestream. QueryId-Methode

Die- `QueryId` Methode ruft einen Bezeichner für die PIN ab.

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

Ein Zeiger auf eine Variable, die eine Zeichenfolge mit dem PIN-Bezeichner empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                       | Beschreibung                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>     | Nicht genügend Arbeitsspeicher.<br/>             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>         | **Null** -Zeigerargument.<br/>       |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Die PIN wurde im Filter nicht gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) -Methode. Um eine Bezeichnerzeichenfolge zu erstellen, ruft die PIN die [**CSource:: findpinnumber**](csource-findpinnumber.md) -Methode mit sich selbst als Parameter auf. Die **findpinnumber** -Methode gibt die von 0 (null) indizierte PIN-Nummer zurück. `QueryId` erhöht den Rückgabewert um 1 und konvertiert das Ergebnis in eine Zeichenfolge. Beispielsweise wird die erste Pin "1". die zweite PIN wird zu "2". und so weiter.

Wenn diese Methode "VFW \_ E \_ nicht gefunden" zurückgibt \_ , gibt Sie an, dass das Array von Pins des Filters ungültig ist, was vermutlich durch einen Fehler im Filter verursacht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




