---
description: Die synchronousblockoutputpin-Methode blockiert die PIN. gibt erst zurück, wenn die PIN blockiert ist.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Cdynamicoutputpin. synchronousblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371336"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>Cdynamicoutputpin. synchronousblockoutputpin-Methode

Die- `SynchronousBlockOutputPin` Methode blockiert die PIN und gibt erst zurück, wenn die PIN blockiert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt> </dl>                   | Die PIN ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt> </dl> | Die PIN ist bereits im aufrufenden Thread blockiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode nicht aus dem streamingthread aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




