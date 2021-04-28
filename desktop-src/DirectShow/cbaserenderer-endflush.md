---
description: 'CBaseRenderer.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: CBaseRenderer.EndFlush-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095908"
---
# <a name="cbaserendererendflush-method"></a>CBaseRenderer.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Der Eingabepin des Filters ruft diese Methode auf, wenn er einen Aufruf der [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




