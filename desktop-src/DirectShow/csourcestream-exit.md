---
description: Die Exit-Methode signalisiert dem streamingthread, den Vorgang zu beenden.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Csourcestream. Exit-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351372"
---
# <a name="csourcestreamexit-method"></a>Csourcestream. Exit-Methode

Die- `Exit` Methode signalisiert dem streamingthread, zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ OK oder E \_ unerwartet zurück.

## <a name="remarks"></a>Bemerkungen

Die [**csourcestream:: inaktive**](csourcestream-inactive.md) -Methode ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




