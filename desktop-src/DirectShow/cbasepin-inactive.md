---
description: 'CBasePin.Inactive-Methode: Die Inaktive Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: CBasePin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099338"
---
# <a name="cbasepininactive-method"></a>CBasePin.Inactive-Methode

Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter beendet wird, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode für alle verbundenen Pins des Filters auf.

Diese Methode führt in der Basisklasse nichts aus. Abgeleitete Klassen sollten diese Methode überschreiben, um alle Ressourcen frei zu lassen, die von der [**CBasePin::Active-Methode erhalten**](cbasepin-active.md) wurden. Zum Beispiel zum Decommit der Zuweisungen des Pins.

Der interne Zustand des Filterdiagramm-Managers wird erst aktualisiert, nachdem diese Methode zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




