---
description: 'Die alterquality-Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird. Diese Methode überschreibt die ctransformfilter:: alterquality-Methode.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Cvideotransformfilter. alterquality-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365379"
---
# <a name="cvideotransformfilteralterquality-method"></a>Cvideotransformfilter. alterquality-Methode

Die- `AlterQuality` Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird. Diese Methode überschreibt die [**ctransformfilter:: alterquality**](ctransformfilter-alterquality.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Q1* 
</dt> <dd>

[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E Fail" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn die Ausgabe-PIN eine Qualitäts Nachricht empfängt (durch die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode).

Der oder bei Verzögerung-Wert aus *q* wird in der **m \_ itrlate** -Member-Variablen gespeichert. Der Rückgabewert von "E \_ Fail" gibt an, dass der Renderer durch das Ablegen von Frames auffangen soll, obwohl die **cvideotransformfilter** -Klasse auch Frames unter den richtigen Bedingungen ablegen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> <dt>

[**Cvideotransformfilter:: schuldskipframe**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




