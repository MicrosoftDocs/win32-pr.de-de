---
description: Die WaitForReceiveToComplete-Methode wartet auf den Abschluss der CBaseRenderer::Receive-Methode.
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: CBaseRenderer.WaitForReceiveToComplete-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1f63efa53cc8e8829aba825e831f95595b16faf97bdf29777918c599aadade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016788"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>CBaseRenderer.WaitForReceiveToComplete-Methode

Die `WaitForReceiveToComplete` -Methode wartet auf den Abschluss der [**CBaseRenderer::Receive-Methode.**](cbaserenderer-receive.md)

## <a name="syntax"></a>Syntax


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**Methoden CBaseRenderer::Stop**](cbaserenderer-stop.md) und [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) rufen diese Methode auf, um die Zustandsänderung mit der **Receive-Methode** zu synchronisieren.

Insbesondere verteilt diese Methode Nachrichten, während sie darauf wartet, dass das [**Flag CBaseRenderer::m \_ bInReceive**](cbaserenderer-m-binreceive.md) zu **FALSE** wird. Das Flag wird in der [**CBaseRenderer::P repareReceive-Methode**](cbaserenderer-preparereceive.md) zu **TRUE** und wechselt zurück zu **FALSE,** nachdem die **Receive-Methode** die [**CBaseRenderer::P repareRender-Methode**](cbaserenderer-preparerender.md) aufruft. Die abgeleitete Klasse kann **PrepareRender** verwenden, um die Palette festzulegen. Wenn Sie auf den Abschluss von **PrepareRender** warten, wird sichergestellt, dass Palettenänderungsmeldungen gesendet werden, bevor die Zustandsänderung erfolgt. Dadurch wird ein potenzieller Deadlock vermieden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




