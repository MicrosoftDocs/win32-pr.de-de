---
description: Die unempfehlung-Methode entfernt eine anforderungsanforderung.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Camschedule. unempfehlung-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371614"
---
# <a name="camscheduleunadvise-method"></a>Camschedule. unempfehlung-Methode

Die- `Unadvise` Methode entfernt eine anforderungsanforderung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwadviabcookie* 
</dt> <dd>

Der Bezeichner der Benachrichtigungs Anforderung, der von der Methode " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) " zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Nicht gefunden<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule. h (Include Streams. h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camschedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




