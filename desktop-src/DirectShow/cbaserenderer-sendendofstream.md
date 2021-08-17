---
description: Wenn das Ende des Streams erreicht wurde, wird von der SendEndOfStream-Methode ein EC \_ COMPLETE-Ereignis für den Filterdiagramm-Manager geplant.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: CBaseRenderer.SendEndOfStream-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 344783d8e8aac755d157f125b02827c9f362ca96271dccb84134f451b31d1bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954819"
---
# <a name="cbaserenderersendendofstream-method"></a>CBaseRenderer.SendEndOfStream-Methode

Wenn das Ende des Streams erreicht wurde, wird von der -Methode ein `SendEndOfStream` EC COMPLETE-Ereignis für den \_ Filterdiagramm-Manager geplant.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Filterdiagramm-Manager akzeptiert keine Ereignisbenachrichtigungen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                                       |



 

## <a name="remarks"></a>Hinweise

Der Filter erhält möglicherweise eine Benachrichtigung zum Streamende vor der Endzeit des aktuellen Beispiels. Wenn dies der Ergebnis ist, sollte der Filter warten, bevor eine [**EC \_ COMPLETE-Benachrichtigung**](ec-complete.md) an den Filtergraph-Manager angezeigt wird.

Deshalb gilt Folgendes:

-   Wenn der Filter eine Early End-of-Stream-Benachrichtigung (EOS) erhalten hat, wird von dieser Methode ein Timerereignis geplant. Wenn das Timerereignis aktiviert ist, veröffentlicht der Filter das EC \_ COMPLETE-Ereignis.
-   Wenn der Filter eine NOCH nicht frühe Benachrichtigung erhalten hat, wird von dieser Methode sofort das EC \_ COMPLETE-Ereignis veröffentlicht.
-   Wenn für den Filter keine ausstehendeN EOS-Benachrichtigungen angezeigt werden, wird die Methode ohne weitere Vorgehensweise zurückgegeben.

Die Timerrückrufmethode ist [**CBaseRenderer::TimerCallback.**](cbaserenderer-timercallback.md) Um das EC \_ COMPLETE-Ereignis zu übermitteln, ruft der Filter die [**CBaseRenderer::NotifyEndOfStream-Methode**](cbaserenderer-notifyendofstream.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




