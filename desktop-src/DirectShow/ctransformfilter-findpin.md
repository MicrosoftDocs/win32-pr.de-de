---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Ctransformfilter. findpin-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364721"
---
# <a name="ctransformfilterfindpin-method"></a>Ctransformfilter. findpin-Methode

Die **findpin** -Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Breit Zeichen-Zeichenfolge, die den PIN-Bezeichner enthält.

</dd> <dt>

*pppin* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN. Wenn die Methode fehlschlägt, `*ppPin` wird auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                       | Beschreibung                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>     | Nicht genügend Arbeitsspeicher.<br/>                       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>         | **Null** -Zeigerargument.<br/>                 |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Es wurde keine PIN mit diesem Bezeichner gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Bei der Implementierung dieser Methode wird [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) nicht so aufgerufen, dass Sie dem PIN-Bezeichner entspricht. Stattdessen geht die Methode davon aus, dass die Eingabe-PIN "in" und die Ausgabe-PIN als "out" bezeichnet wird. Wenn Sie einen anderen Satz von PIN-Bezeichner verwenden, überschreiben Sie diese Methode.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




