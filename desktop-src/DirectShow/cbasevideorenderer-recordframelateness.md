---
description: Mit der recordframellichkeit-Methode wird die Zeit für das Rendering aufgezeichnet und Statistiken für die Eigenschaften Seite gesammelt.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Cbasevideorenderer. recordframel-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359253"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>Cbasevideorenderer. recordframel-Methode

Die `RecordFrameLateness` -Methode zeichnet die Zeit, zu der das Rendering aufgetreten ist, und sammelt Statistiken für die Eigenschaften Seite.

## <a name="syntax"></a>Syntax


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*trlate* 
</dt> <dd>

Der Wert, der angibt, wie spät das Beispiel in Bezugszeit Einheiten über die Fälligkeits Zeit hinausging.

</dd> <dt>

*trframe* 
</dt> <dd>

Interframe-Zeit in Bezugszeit Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




