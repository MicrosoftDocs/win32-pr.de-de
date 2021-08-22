---
description: Die ChangeOutputFormat-Methode ändert dynamisch den Medientyp für die Verbindung und stellt neue Segmentinformationen zur Verfügung.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: CDynamicOutputPin.ChangeOutputFormat-Methode (Amfilter.h)
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
ms.openlocfilehash: 534d588bc1633770c35b0e0edbc2079ed8f7ab5035d3a8d2ff181042d26fdb3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074274"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>CDynamicOutputPin.ChangeOutputFormat-Methode

Die `ChangeOutputFormat` -Methode ändert dynamisch den Medientyp für die Verbindung und stellt neue Segmentinformationen zur Verfügung. Die Änderung kann auftreten, während das Filterdiagramm ausgeführt wird. Sobald diese Methode aufgerufen wurde, können Beispiele mit dem alten Medientyp nicht übermittelt werden. Der Aufrufer muss sicherstellen, dass keine alten Stichproben ausstehen.

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

*Pmt* 
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp angibt.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Startzeit des Segments.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Die Stoppzeit des Segments.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Segmentrate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                           | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Fehler. Möglicherweise hat der besitzende Filter [**CDynamicOutputPin::SetConfigInfo nicht aufruft.**](cdynamicoutputpin-setconfiginfo.md)<br/> |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Die Stecknadel ist nicht verbunden.<br/>                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Diese Methode ändert den Formattyp, während der Filter ausgeführt wird. Wenn der Downstreampin das neue Format akzeptiert, ist keine erneute Verbindung erforderlich. Andernfalls versucht die -Methode, die Verbindung mit dem Pin wiederherzustellen. Wenn die Methode das Format erfolgreich ändert, werden die neuen Segmentinformationen angezeigt. Diese Methode ruft die [**CDynamicOutputPin::ChangeMediaType-Methode**](cdynamicoutputpin-changemediatype.md) auf, um die Formatänderung durchzuführen.

Sie müssen die [**CDynamicOutputPin::StartUsingOutputPin-Methode**](cdynamicoutputpin-startusingoutputpin.md) aufrufen, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




