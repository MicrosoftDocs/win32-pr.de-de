---
description: Die BeginFlush-Methode informiert den besitzenden Filter, um die Downstreamfilter zu leeren. Die abgeleitete Klasse muss diese Methode implementieren.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: CPullPin.BeginFlush-Methode (Pullpin.h)
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
ms.openlocfilehash: d2c7998c1c38a533d67edcd2cc237188a627ec8258a8b0349066e31ecf0fbaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687750"
---
# <a name="cpullpinbeginflush-method"></a>CPullPin.BeginFlush-Methode

Die `BeginFlush` -Methode informiert den besitzenden Filter, um die Downstreamfilter zu leeren. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CPullPin::Seek-Methode**](cpullpin-seek.md) ruft diese Methode auf. Implementieren Sie diese Methode, um die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf jedem downstream-Eingabepin aufzurufen, der Daten von diesem Objekt empfängt. Wenn die Ausgabepins Ihres Filters von [**CBaseOutputPin**](cbaseoutputpin.md)abgeleitet sind, rufen Sie die [**CBaseOutputPin::D eliverBeginFlush-Methode**](cbaseoutputpin-deliverbeginflush.md) auf.

Dieser Entwurf ermöglicht es dem Filter, den Stream einfach durch Aufrufen von **Seek** für das **CPullPin-Objekt** zu suchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




