---
description: Die resetendof Stream-Methode setzt die Flags für das Ende des Streams zurück.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Cbaserderderer. rectendof Stream-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371351"
---
# <a name="cbaserendererresetendofstream-method"></a>Cbaserderderer. rectendof Stream-Methode

Die `ResetEndOfStream` -Methode setzt die Flags für das Ende des Streams zurück.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht die vorherige Bedingung für das Ende des Streams. An diesem Punkt kann der Filter neue Daten empfangen. Die [**cbaserenderer::**](cbaserenderer-stop.md) und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden aufrufen diese Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




