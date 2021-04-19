---
description: Mit der changeoutputformat-Methode wird der Medientyp für die Verbindung dynamisch geändert, und es werden neue Segmentinformationen bereitstellt.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Cdynamicoutputpin. changeoutputformat-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367201"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>Cdynamicoutputpin. changeoutputformat-Methode

Mit der `ChangeOutputFormat` -Methode wird der Medientyp für die Verbindung dynamisch geändert, und es werden neue Segmentinformationen bereitstellt. Die Änderung kann auftreten, während das Filter Diagramm ausgeführt wird. Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden. Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.

</dd> <dt>

*tsegmentstart* 
</dt> <dd>

Die Startzeit des Segments.

</dd> <dt>

*tsegmentbeendet* 
</dt> <dd>

Die Endzeit des Segments.

</dd> <dt>

*dsegmentrate* 
</dt> <dd>

Segment Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                                                                                      |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                | Fehler. Möglicherweise hat der besitzende Filter [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md)nicht aufgerufen.<br/> |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/>                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ändert den Formattyp, während der Filter ausgeführt wird. Wenn die downstreampin das neue Format annimmt, ist keine erneute Verbindung erforderlich. Andernfalls versucht die Methode, die PIN erneut zu verbinden. Wenn die-Methode das Format erfolgreich ändert, werden die neuen Segmentinformationen übermittelt. Diese Methode ruft die [**cdynamicoutputpin:: changemediatype**](cdynamicoutputpin-changemediatype.md) -Methode auf, um die Formatänderung auszuführen.

Sie müssen die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode aufrufen, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




