---
description: 'Die getsyncsource-Methode ruft die Referenzuhr ab, die vom-Objekt verwendet wird. Diese Methode implementiert die imediafilter:: getsyncsource-Methode.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Cbasemediafilter. getsyncsource-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369970"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Cbasemediafilter. getsyncsource-Methode

Die- `GetSyncSource` Methode ruft die Referenzuhr ab, die vom-Objekt verwendet wird. Diese Methode implementiert die [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) -Methode.

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

Wenn das Objekt keine verweisuhr verwendet, wird *\* pclock* auf **null** festgelegt. Wenn **die-** Methode zurückgibt, hat pclock einen ausstehenden Verweis Zähler, wenn *\* pclock* nicht **null** ist. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




