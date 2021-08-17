---
description: Die SourceThreadCanWait-Methode enthält oder gibt den Streamingthread frei.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: CBaseRenderer.SourceThreadCanWait-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba9f8e202d7c98bfea5d7068fa63a8d889d88fb10b4c6a7cb3516fadbca7ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954769"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>CBaseRenderer.SourceThreadCanWait-Methode

Die `SourceThreadCanWait` -Methode enthält oder gibt den Streamingthread frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCanWait* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Streamingthread verwendet werden soll. True **gibt an,** dass der Streamingthread blockiert wird, während der Filter darauf wartet, die nächsten Beispiele zu rendern. False **gibt an,** dass der Streamingthread freigegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Das Aufrufen der -Methode mit dem Wert FALSE zwingt den Filter, von einem blockierten `SourceThreadCanWait` [**IMemInputPin::Receive-Aufruf zurückzukehren.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)  Wenn der Filter ausgeführt wird, blockiert er **Empfangsaufrufe** bis zur Präsentationszeit des aktuellen Beispiels. Wenn der Filter angehalten wird, werden **Empfangsaufrufe** unbegrenzt blockiert. Dieses Verhalten reguliert den Datenfluss im Stream. Wenn der Filter beendet oder geleert wird, sollte er jedoch nicht blockiert werden.

Die Blockierung wird von der [**CBaseRenderer::WaitForRenderTime-Methode**](cbaserenderer-waitforrendertime.md) gesteuert, die auf zwei Ereignisse wartet: [**CBaseRenderer::m \_ RenderEvent**](cbaserenderer-m-renderevent.md) und [**CBaseRenderer::m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md). Das **m \_ RenderEvent-Ereignis** wird signalisiert, wenn die Präsentationszeit eintrifft. Das **m \_ ThreadSignal-Ereignis** wird signalisiert, `SourceThreadCanWait` wenn mit dem Wert FALSE aufgerufen **wird.** Wenn `SourceThreadCanWait` Sie mit dem Wert TRUE **aufrufen,** wird das Ereignis zurückgesetzt.

Die [**Methoden CBaseRenderer::Stop**](cbaserenderer-stop.md) und [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) rufen mit dem Wert `SourceThreadCanWait` **FALSE** auf (freigeben des Streamingthreads). Die [**Methoden CBaseRenderer::P ause,**](cbaserenderer-pause.md) [**CBaseRenderer::Run**](cbaserenderer-run.md)und [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) rufen mit dem Wert `SourceThreadCanWait` TRUE **auf.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




