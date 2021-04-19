---
description: Die preparereceive-Methode bereitet den Filter zum Rendering eines Beispiels vor.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Cbaserderderer. preparereceive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367135"
---
# <a name="cbaserendererpreparereceive-method"></a>Cbaserderderer. preparereceive-Methode

Die- `PrepareReceive` Methode bereitet den Filter zum Rendering eines Beispiels vor.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                             | Beschreibung                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                        |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                  | Fehler.<br/>                         |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>            | Unerwarteter Fehler.<br/>               |
| <dl> <dt>**VFW \_ E- \_ Beispiel \_ abgelehnt**</dt> </dl> | Das Beispiel wird vom Filter gelöscht.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Filter ruft diese Methode innerhalb der [**cbaserenderer:: Receive**](cbaserenderer-receive.md) -Methode auf, bevor ein Beispiel gerendert wird. Wenn der Filter ausgeführt wird, plant diese Methode das Beispiel für das Rendering.

Wenn für den Filter bereits ein ausstehendes Beispiel vorhanden ist, oder wenn das Ende des Streams bereits erreicht wurde, gibt die Methode "E unerwartete" zurück \_ . Der Upstream-Filter serialisiert seine Streamingaufrufe möglicherweise nicht ordnungsgemäß.

Wenn der Zeit Planungs Algorithmus feststellt, dass das Beispiel gelöscht werden soll (siehe [**cbaserenderer:: schedulesample**](cbaserenderer-schedulesample.md)), gibt die Methode VFW \_ E \_ Sample zurück \_ . Die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der Eingabe-PIN übergibt diesen Fehlercode jedoch nicht an den upstreamfilter, da das Ablegen eines Beispiels kein Fehler ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




