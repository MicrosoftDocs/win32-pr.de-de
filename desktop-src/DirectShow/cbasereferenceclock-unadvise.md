---
description: 'Die unempfehlung-Methode entfernt eine ausstehende Benachrichtigungs Anforderung. Diese Methode implementiert die IReferenceClock:: unberatungsmethode.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: Cbasereferenceclock. unempfehlung-Methode (Ref. h)
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
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372702"
---
# <a name="cbasereferenceclockunadvise-method"></a>Cbasereferenceclock. unempfehlung-Methode

Die- `Unadvise` Methode entfernt eine ausstehende Benachrichtigungs Anforderung. Diese Methode implementiert die [**IReferenceClock:: unberatungsmethode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

## <a name="syntax"></a>Syntax


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwadviabtoken* 
</dt> <dd>

Der Bezeichner der zu entfernenden Anforderung. Verwenden Sie den Wert, der von den Methoden [**cbasereferenceclock:: advientime**](cbasereferenceclock-advisetime.md) oder [**cbasereferenceclock:: advi\periodisch**](cbasereferenceclock-adviseperiodic.md) im *pdwadvictoken* -Parameter zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Nicht gefunden:<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




