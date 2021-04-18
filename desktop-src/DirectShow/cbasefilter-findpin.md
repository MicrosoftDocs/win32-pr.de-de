---
description: 'Die findpin-Methode ruft die PIN mit dem angegebenen Bezeichner ab. Diese Methode implementiert die ibasefilter:: findpin-Methode.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Cbasefilter. findpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360927"
---
# <a name="cbasefilterfindpin-method"></a>Cbasefilter. findpin-Methode

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

Zeiger auf eine Konstante, mit NULL endender Unicode-Zeichenfolge, die die PIN identifiziert.

</dd> <dt>

*pppin* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                       | Beschreibung                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>         | **Null** -Zeigerargument.<br/>     |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Es konnte keine passende Pin gefunden werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbasepin:: Name**](cbasepin-name.md) -Methode auf, um den Namen jeder PIN mit der durch den *ID* -Parameter angegebenen Zeichenfolge zu vergleichen.

Wenn die Methode erfolgreich ausgeführt wird, hat die **IPin** -Schnittstelle einen ausstehenden Verweis Zähler. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




