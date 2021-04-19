---
description: Die Run-Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Cbasepin. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369711"
---
# <a name="cbasepinrun-method"></a>Cbasepin. Run-Methode

Die- `Run` Methode benachrichtigt die PIN, dass der Filter jetzt ausgeführt wird.

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

Die Startzeit, die an die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode des Filters übermittelt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter von "angehalten" in "wird ausgeführt" wechselt, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode für alle Pins des Filters auf.

Diese Methode führt in der Basisklasse keine Aktion aus. Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann eine PIN einen Arbeits Thread starten, der Beispiele liefert.

Der interne Zustand des Filter Graph-Managers wird erst aktualisiert, nachdem diese Element Funktion zurückgegeben wurde. Testen Sie daher nicht den Status dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




