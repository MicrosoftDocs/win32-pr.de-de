---
description: Die prepareperformancedata-Methode legt die m \_ trlate-und m \_ trframe-Werte des aktuellen Frames fest.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Cbasevideorenderer. prepareperformancedata-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369967"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Cbasevideorenderer. prepareperformancedata-Methode

Die `PreparePerformanceData` -Methode legt die **m \_ trlate** -und **m \_ trframe** -Werte des aktuellen Frames fest.

## <a name="syntax"></a>Syntax


```C++
void PreparePerformanceData(
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

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion **legt \_ m trlate** auf den Wert von *trlate* und **m \_ trframe** auf den Wert von *trframe* fest.

Wenn die Member-Funktion [**cbasevideorenderer:: recordframellichkeit**](cbasevideorenderer-recordframelateness.md) von [**cbasevideorenderer:: onrenderstart**](cbasevideorenderer-onrenderstart.md) oder [**cbasevideorenderer:: ondirectrender**](cbasevideorenderer-ondirectrender.md)aufgerufen wird, werden die Werte von **m \_ trlate** und **m \_ trframe** übergeben, um die Statistiken zu aktualisieren. `PreparePerformanceData` wird von [**cbasevideorenderer:: onwaitend**](cbasevideorenderer-onwaitend.md) aufgerufen, um diese Datenmember-Werte festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




