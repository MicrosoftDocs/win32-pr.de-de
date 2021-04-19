---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource. findpin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355892"
---
# <a name="csourcefindpin-method"></a>CSource. findpin-Methode

Die- `FindPin` Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) -Methode.

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

Zeiger auf eine mit NULL endenden Zeichenfolge, die die PIN identifiziert.

</dd> <dt>

*pppin* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN. Wenn die Methode fehlschlägt, \* wird *pppin* auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                       | Beschreibung                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>         | **Null** -Zeigerargument.<br/>                 |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Es wurde keine PIN mit diesem Bezeichner gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die erste Pin hat immer den Namen "1". die zweite Pin hat den Namen "2". und so weiter. Weitere Informationen finden Sie unter [**csourcestream:: QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




