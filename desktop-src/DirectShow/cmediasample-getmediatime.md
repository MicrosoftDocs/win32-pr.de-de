---
description: 'Die getmediatime-Methode ruft die Medien Zeiten für dieses Beispiel ab. Diese Methode implementiert die imediasample:: getmediatime-Methode.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Cmediasample. getmediatime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364881"
---
# <a name="cmediasamplegetmediatime-method"></a>Cmediasample. getmediatime-Methode

Die- `GetMediaTime` Methode ruft die Medien Zeiten für dieses Beispiel ab. Diese Methode implementiert die [**imediasample:: getmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Start Zeit der Medien empfängt.

</dd> <dt>

*ausgesetzt* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit des Mediums empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                  | Beschreibung                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ Medien \_ Zeit \_ nicht \_ festgelegt**</dt> </dl> | Für dieses Beispiel wurden keine Medien Zeiten festgelegt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die [**cmediasample:: m \_ mediaend**](cmediasample-m-mediaend.md) -Member-Variable gibt einen Offset von [**cmediasample:: m \_ mediastart**](cmediasample-m-mediastart.md)an, aber der vom *Pend* -Parameter empfangene Wert ist eine absolute Medien Zeit, berechnet als **m \_ mediastart**  +  **m \_ mediaend**.

Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




