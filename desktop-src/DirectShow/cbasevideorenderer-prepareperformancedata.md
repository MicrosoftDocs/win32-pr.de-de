---
description: Die PreparePerformanceData-Methode legt die m \_ trLate- und m \_ trFrame-Werte des aktuellen Frames fest.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: CBaseVideoRenderer.PreparePerformanceData-Methode (Renbase.h)
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
ms.openlocfilehash: e8cb276b37e64b6bb34751ed2d034666f7ceeddd90d8e52e47b2a1fca499ff9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658334"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>CBaseVideoRenderer.PreparePerformanceData-Methode

Die `PreparePerformanceData` -Methode legt die **TrFrame-Werte m \_ trLate** und **\_ m** des aktuellen Frames fest.

## <a name="syntax"></a>Syntax


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*trLate* 
</dt> <dd>

Wert, der angibt, wie spät die Stichprobe über die Fälligkeitszeit hinaus war (in Referenzzeiteinheiten).

</dd> <dt>

*trFrame* 
</dt> <dd>

Interframe-Zeit in Referenzzeiteinheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion legt **m \_ trLate auf** den Wert von *trLate und* m **\_ trFrame** auf den Wert *von trFrame fest.*

Wenn die [**CBaseVideoRenderer::RecordFrameLateness-Memberfunktion**](cbasevideorenderer-recordframelateness.md) entweder von [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) oder [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md)aufgerufen wird, übergibt sie die Werte **von m \_ trLate** und **m \_ trFrame,** damit die Statistik aktualisiert wird. `PreparePerformanceData` wird von [**CBaseVideoRenderer::OnWaitEnd aufgerufen,**](cbasevideorenderer-onwaitend.md) um diese Datenmitgliedswerte zu festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




