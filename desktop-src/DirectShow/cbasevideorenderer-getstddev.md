---
description: Die getstddev-Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, an dem jeder Frame fällig ist, und dem Zeitpunkt, zu dem er tatsächlich gerendert wird, für Statistiken pro Frame.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Cbasevideorenderer. getstddev-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358009"
---
# <a name="cbasevideorenderergetstddev-method"></a>Cbasevideorenderer. getstddev-Methode

Die `GetStdDev` -Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, an dem jeder Frame fällig ist, und dem tatsächlichen Rendering für pro-Frame-Statistik.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nsamples* 
</dt> <dd>

Ganzzahliger Wert, der die Anzahl der Videobeispiele enthält, die vom Videorenderer empfangen wurden.

</dd> <dt>

*piresult* 
</dt> <dd>

Ein Zeiger auf einen ganzzahligen Wert, der die Standardabweichung enthalten soll.

</dd> <dt>

*llsumsq* 
</dt> <dd>

Ein Wert, der die Standardabweichung aller gerenderten Videobeispiele in Millisekunden darstellt. Je niedriger der Wert, desto konsistent ist das Rendering.

</dd> <dt>

*itot* 
</dt> <dd>

Ein Wert, der den Mittelwert (in Millisekunden) zwischen der gestempelten Zeit und der gerenderten Zeit für alle gerenderten Videobeispiele darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt noError zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




