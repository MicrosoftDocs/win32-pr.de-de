---
description: Die SendQuality-Methode sendet eine Qualitätsnachricht, um anzugeben, welche Maßnahmen der Anbieter zur Qualität unternehmen soll.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: CBaseVideoRenderer.SendQuality-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074764"
---
# <a name="cbasevideorenderersendquality-method"></a>CBaseVideoRenderer.SendQuality-Methode

Die `SendQuality` -Methode sendet eine Qualitätsmeldung, um anzugeben, was der Anbieter in Der Qualität tun soll.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*trLate* 
</dt> <dd>

Die Zeit, um die der Frame zu spät ist.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Currentstreamzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion sendet eine Qualitätskontrollnachricht vorgelagert, um das Qualitätsmanagement zu steuern. Die Art der Qualitätsmeldung (d. h. ob die Anzahl der Stichproben reduziert oder erhöht werden soll) wird in der Implementierung des Qualitätsmanagements in dieser abgeleiteten Klasse bestimmt (siehe [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




