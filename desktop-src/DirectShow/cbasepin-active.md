---
description: Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Cbasepin. Active-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369180"
---
# <a name="cbasepinactive-method"></a>Cbasepin. Active-Methode

Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter von "angehalten" in "angehalten" wechselt, ruft die [**cbasefilter**](cbasefilter.md) -Klasse diese Methode auf allen verbundenen Pins des Filters auf.

Diese Methode führt in der Basisklasse keine Aktion aus. Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann eine PIN einen Commit für Zuordnungen durchsetzen oder Hardware Ressourcen abrufen.

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

 

 




