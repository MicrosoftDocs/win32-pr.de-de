---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Cbasepin. Notify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357693"
---
# <a name="cbasepinnotify-method"></a>Cbasepin. Notify-Methode

Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pself* 
</dt> <dd>

Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters, der die Qualitäts Steuerungs Meldung übermittelt hat.

</dd> <dt>

*Q1* 
</dt> <dd>

Gibt eine [**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur an, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklasse gibt E \_ notimpl zurück.

## <a name="remarks"></a>Bemerkungen

Ausgabe Pins sollten diese Methode überschreiben, um Qualitäts Steuerungs Meldungen zu akzeptieren.

Wenn ein externer Quality Manager installiert wurde (siehe [**cbasepin:: setsink**](cbasepin-setsink.md)), übergeben Sie die Nachricht an diesen Quality Manager. Andernfalls sollte der Filter die Nachricht selbst verarbeiten oder die Nachrichten-upstreamnachricht übergeben. Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




