---
description: Die beginflush-Methode informiert den besitzenden Filter, um die downstreamfilter zu leeren. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Cpullpin. beginflush-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359391"
---
# <a name="cpullpinbeginflush-method"></a>Cpullpin. beginflush-Methode

Die- `BeginFlush` Methode informiert den besitzenden Filter, um die downstreamfilter zu leeren. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cpullpin:: Seek**](cpullpin-seek.md) -Methode ruft diese Methode auf. Implementieren Sie diese Methode, um die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt. Wenn die Ausgabe-PIN (s) Ihres Filters von [**cbaseoutputpin**](cbaseoutputpin.md)abgeleitet ist, rufen Sie die [**cbaseoutputpin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) -Methode auf.

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

 

 




