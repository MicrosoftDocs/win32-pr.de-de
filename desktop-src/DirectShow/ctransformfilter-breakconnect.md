---
description: Die breakconnect-Methode gibt eine PIN von einer Verbindung frei.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Ctransformfilter. breakconnect-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372271"
---
# <a name="ctransformfilterbreakconnect-method"></a>Ctransformfilter. breakconnect-Methode

Die- `BreakConnect` Methode gibt eine PIN von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dir* 
</dt> <dd>

Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) , der angibt, welche Pin-Verbindung unterbrochen wurde (Eingabe oder Ausgabe).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: breakconnect**](ctransforminputpin-breakconnect.md) -Methode und die [**ctransformoutputpin:: breakconnect**](ctransformoutputpin-breakconnect.md) -Methode ruft diese Methode auf, wenn eine PIN-Verbindung unterbrochen wird. Diese Methode führt in der Basisklasse keine Aktion aus. Wenn Sie die [**checkConnect**](ctransformfilter-checkconnect.md) -Methode überschreiben, überschreiben Sie diese Methode, um alle Ressourcen freizugeben, die in der **checkConnect** -Methode (einschließlich Schnittstellen Zeigern)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




