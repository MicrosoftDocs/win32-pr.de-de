---
description: Die sourcethreadcanwait-Methode enthält den streamingindthread oder gibt diesen frei.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Cbaserderderer. sourcethreadcanwait-Methode (renbase. h)
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
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367114"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Cbaserderderer. sourcethreadcanwait-Methode

Die- `SourceThreadCanWait` Methode enthält den streamingthread oder gibt diesen frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bcanwait* 
</dt> <dd>

Boolescher Wert, der angibt, ob der streamingthread enthalten sein soll. **True** gibt an, dass der streamingingthread blockiert wird, während der Filter auf das Rendering der nächsten Beispiele wartet. Wenn **false**, wird der streamingingthread freigegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die- `SourceThreadCanWait` Methode mit dem Wert **false** aufrufen, wird der Filter gezwungen, von einem blockierten [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Aufruf zurückzukehren. Wenn der Filter ausgeführt wird, werden **Empfangs** Aufrufe bis zum Präsentations Zeitpunkt des aktuellen Beispiels blockiert. Wenn der Filter angehalten wird, werden **Empfangs** Aufrufe unbegrenzt blockiert. Dieses Verhalten regelt den Datenfluss im Stream. Wenn der Filter beendet oder geleert wird, sollte er jedoch nicht blockiert werden.

Die Blockierung wird von der [**cbaserdenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md) -Methode gesteuert, die auf zwei Ereignisse wartet: [**cbaserdenderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) und [**cbasererderer:: m \_ threadsignal**](cbaserenderer-m-threadsignal.md). Das **m \_ renderevent** -Ereignis wird signalisiert, wenn die Präsentationszeit erreicht wird. Das **m \_ threadsignal** -Ereignis wird signalisiert, wenn `SourceThreadCanWait` mit dem Wert **false** aufgerufen wird. `SourceThreadCanWait`Wenn Sie mit dem Wert **true** aufrufen, wird das-Ereignis zurückgesetzt.

Die [**cbaserenderer:: Ende**](cbaserenderer-stop.md) -und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden aufrufen `SourceThreadCanWait` mit dem Wert **false** (Freigabe des streaminginthreads). Der [**cbaserenumderer::P ause**](cbaserenderer-pause.md), [**cbasererderderer:: Run**](cbaserenderer-run.md)-Methode und der [**cbaserderderer:: endflush**](cbaserenderer-endflush.md) -Methodenaufrufe `SourceThreadCanWait` mit dem Wert " **true**".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




