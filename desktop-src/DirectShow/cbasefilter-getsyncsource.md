---
description: 'Die getsyncsource-Methode ruft die Referenzuhr ab, die der Filter verwendet. Diese Methode implementiert die imediafilter:: getsyncsource-Methode.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Cbasefilter. getsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371484"
---
# <a name="cbasefiltergetsyncsource-method"></a>Cbasefilter. getsyncsource-Methode

Die- `GetSyncSource` Methode ruft die Referenzuhr ab, die vom Filter verwendet wird. Diese Methode implementiert die [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclock* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Uhr empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter keine verweisuhr verwendet, wird *\* pclock* auf **null** festgelegt. Wenn **die-** Methode zurückgibt, hat pclock einen ausstehenden Verweis Zähler, wenn *\* pclock* nicht **null** ist. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




