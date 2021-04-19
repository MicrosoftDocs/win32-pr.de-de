---
description: Die setsyncsource-Methode benachrichtigt die Basisklasse der aktuellen verweisuhr.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Cbasestreamcontrol. setsyncsource-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355863"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a>Cbasestreamcontrol. setsyncsource-Methode

Die- `SetSyncSource` Methode benachrichtigt die Basisklasse der aktuellen verweisuhr.

## <a name="syntax"></a>Syntax


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*präfemuhr* 
</dt> <dd>

Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle der Referenzuhr.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Aufrufen Sie diese Methode in der [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode des Filters. Die **cbasestreamcontrol** -Klasse verwendet die **IReferenceClock** -Schnittstelle, um sicherzustellen, dass die Stichproben nicht zu schnell verworfen werden.

## <a name="examples"></a>Beispiele


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




