---
description: Die onthreadstartplay-Methode wird am Anfang der csourcestream::D obufferprocessingloop-Methode aufgerufen.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Csourcestream. onthreadstartplay-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369144"
---
# <a name="csourcestreamonthreadstartplay-method"></a>Csourcestream. onthreadstartplay-Methode

Die- `OnThreadStartPlay` Methode wird zu Beginn der [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode führt in der Basisklasse keine Aktion aus. Sie kann von der abgeleiteten Klasse außer Kraft gesetzt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




