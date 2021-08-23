---
description: Die Run-Methode benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird. Diese Methode überschreibt die CBasePin::Run-Methode.
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: CRenderedInputPin.Run-Methode (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c372101aee2817e08545080048c98a25af7efb152f4873e54366e73571763065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652020"
---
# <a name="crenderedinputpinrun-method"></a>CRenderedInputPin.Run-Methode

Die `Run` -Methode benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird. Diese Methode überschreibt die [**CBasePin::Run-Methode.**](cbasepin-run.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Die Startzeit, die an die [**IMediaFilter::Run-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) des Filters übergeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRenderedInputPin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




