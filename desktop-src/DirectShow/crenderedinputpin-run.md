---
description: 'Die Run-Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird. Diese Methode überschreibt die cbasepin:: Run-Methode.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Crenderedinputpin. Run-Methode (amextra. h)
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
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354208"
---
# <a name="crenderedinputpinrun-method"></a>Crenderedinputpin. Run-Methode

Die- `Run` Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird. Diese Methode überschreibt die [**cbasepin:: Run**](cbasepin-run.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tSTART* 
</dt> <dd>

Die Startzeit, die an die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode des Filters übermittelt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crenderedinputpin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




