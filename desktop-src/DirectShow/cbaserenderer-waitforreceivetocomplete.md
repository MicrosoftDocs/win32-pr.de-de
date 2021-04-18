---
description: 'Die waitforreceivetocomplete-Methode wartet auf den Abschluss der cbaserdenderer:: Receive-Methode.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Cbaserderderer. waitforreceivetocomplete-Methode (renbase. h)
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
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358202"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Cbaserderderer. waitforreceivetocomplete-Methode

Die- `WaitForReceiveToComplete` Methode wartet auf den Abschluss der [**cbaserdenderer:: Receive**](cbaserenderer-receive.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit den [**cbaserenderer::**](cbaserenderer-stop.md) und [**cbaserenderer:: beginflush**](cbaserenderer-beginflush.md) -Methoden wird diese Methode aufgerufen, um die Zustandsänderung mit der **Receive** -Methode zu synchronisieren.

Diese Methode sendet Nachrichten, während Sie darauf wartet, dass das [**cbaserdenderer:: m \_ binreceive**](cbaserenderer-m-binreceive.md) -Flag auf " **false**" wird. Das Flag wird in der [**cbaserererererererermethode**](cbaserenderer-preparereceive.md) " **true** "::P der Analysemethode "" und wechselt zurück zu " **false** ", nachdem die **Receive** -Methode die [**cbasererderderer**](cbaserenderer-preparerender.md) -Methode aufgerufen hat::P Die abgeleitete Klasse kann **preparerender** zum Festlegen der Palette verwenden. Durch das warten auf den Abschluss der **Vorbereitung** wird sichergestellt, dass palettenänderungs Meldungen vor der Zustandsänderung weitergeleitet werden. Dadurch wird ein potenzieller Deadlock vermieden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




