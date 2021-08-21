---
description: Die StopStreaming-Methode hält das Streaming an, wenn der Filter den Ausführungsstatus ausschaltet.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: CBaseRenderer.StopStreaming-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097ad9fd1548b709f7eb74a3e468c34c3b18a73621720e249a3c626c252c898d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016798"
---
# <a name="cbaserendererstopstreaming-method"></a>CBaseRenderer.StopStreaming-Methode

Die `StopStreaming` -Methode hält das Streaming an, wenn der Filter den Ausführungsstatus ausschaltet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBaseRenderer::OnStopStreaming-Methode auf.**](cbaserenderer-onstopstreaming.md) Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




