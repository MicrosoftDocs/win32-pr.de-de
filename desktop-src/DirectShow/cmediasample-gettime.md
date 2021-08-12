---
description: Die GetTime-Methode ruft die Streamzeiten ab, zu denen dieses Beispiel beginnen und abgeschlossen werden soll. Diese Methode implementiert die IMediaSample::GetTime-Methode.
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: CMediaSample.GetTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 755965864692cf2b34ebaadc6e064a47a7514c69fe891a6a15f1bb364e5345e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655251"
---
# <a name="cmediasamplegettime-method"></a>CMediaSample.GetTime-Methode

Die `GetTime` -Methode ruft die Streamzeiten ab, zu denen dieses Beispiel beginnen und abgeschlossen werden soll. Diese Methode implementiert die [**IMediaSample::GetTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Anfangszeit des Streams in Einheiten von 100 Nanosekunden empfängt.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Zeiger auf eine Variable, die die Endstreamzeit in Einheiten von 100 Nanosekunden empfängt. Wenn das Beispiel keine Stoppzeit auf hat, wird der Wert auf die Startzeit plus 1 festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                   | Beschreibung                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Erfolg.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ NO \_ STOP \_ TIME**</dt> </dl>         | Das Beispiel hat eine gültige Startzeit, aber keine Stoppzeit.<br/> |
| <dl> <dt>**VFW \_ E \_ SAMPLE \_ TIME \_ NOT \_ SET**</dt> </dl> | Das Beispiel enthält keine gültigen Zeitstempel.<br/>          |



 

## <a name="remarks"></a>Hinweise

Die [**Membervariablen CMediaSample::m \_ Start**](cmediasample-m-start.md) und [**CMediaSample::m \_ End**](cmediasample-m-end.md) geben die Zeitstempel an. Die [**CMediaSample::m \_ dwFlags-Membervariable**](cmediasample-m-dwflags.md) gibt an, ob die Zeitstempel gültig sind.

Informationen zu Zeitstempeln finden Sie unter [Zeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




