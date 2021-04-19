---
description: Wenn das Ende des Streams erreicht wurde, plant die Methode "sendendof Stream" ein EC \_ Complete-Ereignis für den Filter Graph-Manager.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Cbaserderderer. sendendof Stream-Methode (renbase. h)
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
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372310"
---
# <a name="cbaserenderersendendofstream-method"></a>Cbaserderderer. sendendof Stream-Methode

Wenn das Ende des Streams erreicht wurde, plant die- `SendEndOfStream` Methode ein EC \_ Complete-Ereignis für den Filter Graph-Manager.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Der Filter Graph-Manager akzeptiert keine Ereignis Benachrichtigungen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Der Filter erhält möglicherweise vor der Endzeit des aktuellen Beispiels eine Benachrichtigung über das Ende des Datenstroms. Wenn dies der Fall ist, sollte der Filter warten, bevor er eine [**EC \_ Complete**](ec-complete.md) -Benachrichtigung an den Filter Graph-Manager veröffentlicht.

Deshalb gilt Folgendes:

-   Wenn der Filter eine frühe End-of-Stream-Benachrichtigung (EOS) empfangen hat, plant diese Methode ein Timer-Ereignis. Wenn das Timer-Ereignis aktiviert ist, stellt der Filter das EC Complete-Ereignis zur Verfügung \_ .
-   Wenn der Filter eine nicht frühe EOS-Benachrichtigung erhalten hat, sendet diese Methode sofort das EC \_ Complete-Ereignis.
-   Wenn der Filter keine ausstehende EOS-Benachrichtigung hat, gibt die Methode zurück, ohne etwas zu tun.

Die Timer-Rückruf Methode ist [**cbasererderderer:: TimerCallback**](cbaserenderer-timercallback.md). Um das EC Complete-Ereignis zu übermitteln \_ , ruft der Filter die [**cbaserdenderer:: notifyendofstream**](cbaserenderer-notifyendofstream.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




