---
description: Die endflush-Methode informiert den besitzenden Filter, einen Leerungs Vorgang zu beenden. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Cpullpin. endflush-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371257"
---
# <a name="cpullpinendflush-method"></a>Cpullpin. endflush-Methode

Die- `EndFlush` Methode informiert den besitzenden Filter, um einen Leerungs Vorgang zu beenden. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cpullpin:: Seek**](cpullpin-seek.md) -Methode ruft diese Methode auf. Implementieren Sie diese Methode, um die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt. Wenn die Ausgabe-PIN (s) Ihres Filters von **cbaseoutputpin** abgeleitet ist, rufen Sie die **cbaseoutputpin::D eliverendflush** -Methode auf.

Dieser Entwurf ermöglicht dem Filter, einfach durch Aufrufen von **Seek** im **cpullpin** -Objekt auf den Stream zu suchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




