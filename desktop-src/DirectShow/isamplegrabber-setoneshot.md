---
description: Die SetOneShot-Methode gibt an, ob der Sample Grabber-Filter anzuhalten ist, nachdem der Filter eine Stichprobe empfangen hat.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: ISampleGrabber::SetOneShot-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7829bd57cb2d813f71e17a4925d6e5fab7cc34330041461b691e00eae6ca5cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817681"
---
# <a name="isamplegrabbersetoneshot-method"></a>ISampleGrabber::SetOneShot-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die **SetOneShot-Methode** gibt an, ob der [**Sample Grabber-Filter**](sample-grabber-filter.md) anzuhalten ist, nachdem der Filter eine Stichprobe empfangen hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Oneshot* 
</dt> <dd>

Ein boolescher Wert, der angibt, ob der Sample Grabber-Filter nach dem Empfang eines Beispiels anzuhalten ist.



| Wert                                                                                                                                    | Bedeutung                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE!</dt> </dl>    | Das Beispielgrab wird nach der ersten Stichprobe anzuhalten. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE!</dt> </dl> | Nach dem ersten Beispiel werden die Stichproben weiterhin vom Beispielgrabber verwendet. Dies ist das Standardverhalten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um wie folgt ein einzelnes Beispiel aus dem Stream zu erhalten:

1.  Rufen **Sie SetOneShot mit** dem Wert TRUE **auf.**
2.  Verwenden Sie optional die [**IMediaSeeking-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) um nach einer Position im Stream zu suchen.
3.  Rufen [**Sie IMediaControl::Run auf,**](/windows/desktop/api/Control/nf-control-imediacontrol-run) um das Filterdiagramm ausführen.
4.  Rufen [**Sie IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) auf, um auf das Anhalten des Graphen zu warten. Rufen Sie alternativ [**IMediaEvent::GetEvent auf,**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) um Graphereignisse zu erhalten, bis Sie das [**EC \_ COMPLETE-Ereignis**](ec-complete.md) erhalten.

Nach dem Anhalten des Beispielgrabbers befindet sich das Filterdiagramm noch in einem ausgeführten Zustand. Sie können das Diagramm suchen oder anhalten, um ein weiteres Beispiel zu erhalten.

> [!Note]  
> In einer früheren Version der Dokumentation wurde angegeben, dass das Filterdiagramm nach dem Empfangen des Beispiels beendet wird. Das ist nicht genau. Der Stream endet, aber das Diagramm bleibt im Ausführungszustand.

 

Der Sample Grabber implementiert den einmal ausgeführten Modus, indem [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) für den Downstreamfilter aufruft und S FALSE von der \_ [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) des Filters zurückgegeben wird.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden des Beispielgrabbers](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




