---
description: Die GetStdDev-Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, zu dem jeder Frame fällig ist, und dem Zeitpunkt, zu dem er tatsächlich gerendert wird, für statistiken pro Frame.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: CBaseVideoRenderer.GetStdDev-Methode (Renbase.h)
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
ms.openlocfilehash: 5f7b6ab85000f537179fcc9ae6b979194ae4e975ea2b394d0c58afb8515158aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157082"
---
# <a name="cbasevideorenderergetstddev-method"></a>CBaseVideoRenderer.GetStdDev-Methode

Die `GetStdDev` -Methode schätzt die Standardabweichung in Millisekunden zwischen dem Zeitpunkt, zu dem jeder Frame fällig ist, und dem Zeitpunkt, zu dem er tatsächlich gerendert wird, für die Pro-Frame-Statistik.

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

*nSamples* 
</dt> <dd>

Ganzzahliger Wert, der die Anzahl der vom Videorenderer empfangenen Videobeispiele enthält.

</dd> <dt>

*piResult* 
</dt> <dd>

Zeiger auf einen ganzzahligen Wert, der die Standardabweichung enthält.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Wert, der die Standardabweichung aller gerenderten Videobeispiele in Millisekunden darstellt. Je niedriger der Wert, desto konsistenter ist das Rendering.

</dd> <dt>

*iTot* 
</dt> <dd>

Ein Wert, der den Mittelwert in Millisekunden zwischen der zeitstempelten Zeit und der gerenderten Zeit für alle gerenderten Videobeispiele darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NOERROR zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




