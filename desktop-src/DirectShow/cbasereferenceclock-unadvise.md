---
description: Die Unadvise-Methode entfernt eine ausstehende Advise-Anforderung. Diese Methode implementiert die IReferenceClock::Unadvise-Methode.
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: CBaseReferenceClock.Unadvise-Methode (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652450"
---
# <a name="cbasereferenceclockunadvise-method"></a>CBaseReferenceClock.Unadvise-Methode

Die `Unadvise` -Methode entfernt eine ausstehende Advise-Anforderung. Diese Methode implementiert die [**IReferenceClock::Unadvise-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise)

## <a name="syntax"></a>Syntax


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

Bezeichner der zu entfernenden Anforderung. Verwenden Sie den Wert, der von den [**Methoden CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) oder [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) im *pdwAdviseToken-Parameter zurückgegeben* wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Nicht gefunden:<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




