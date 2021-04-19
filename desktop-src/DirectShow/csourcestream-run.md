---
description: Die Run-Methode signalisiert, dass der streamingthread ausgeführt werden soll.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Csourcestream. Run-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361687"
---
# <a name="csourcestreamrun-method"></a>Csourcestream. Run-Methode

Die- `Run` Methode signalisiert dem streamingthread, ausgeführt zu werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ OK oder E \_ unerwartet zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse hat diese Methode dieselbe Wirkung wie die [**csourcestream::P ause**](csourcestream-pause.md) -Anforderung und wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




