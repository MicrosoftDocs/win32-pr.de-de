---
description: Bestimmt, ob ein Quell Rechteck gültig ist.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Cbasecontrolvideo. checksourcerect-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366055"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a>Cbasecontrolvideo. checksourcerect-Methode

Bestimmt, ob ein Quell Rechteck gültig ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourcerect* 
</dt> <dd>

Zeiger auf das zu Überprüfung des Quell Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ invalidArg" zurück, wenn es ungültig ist; andernfalls wird "noError (S OK)" zurückgegeben \_ .

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion überprüft, ob das angeforderte Quell Rechteck das verfügbare Quellvideo nicht überschreitet. Die linke und die obere Koordinate dürfen nicht negativ sein, und die Breite und die Höhe dürfen nicht den rechten und unteren Rand des Videos überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




