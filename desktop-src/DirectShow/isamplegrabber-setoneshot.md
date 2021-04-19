---
description: Die Methode "-Methode" gibt an, ob der Sample Grabber-Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Isamplegrabber:: setoneshot-Methode (qedit. h)'
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
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360419"
---
# <a name="isamplegrabbersetoneshot-method"></a>Isamplegrabber:: setoneshot-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **Methode "** -Methode" gibt an, ob der [**Sample Grabber**](sample-grabber-filter.md) -Filter angehalten wird, nachdem der Filter ein Beispiel erhalten hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OneShot* 
</dt> <dd>

Ein boolescher Wert, der angibt, ob der Sample-Grabber Filter nach dem Empfang eines Beispiels angehalten wird.



| Wert                                                                                                                                    | Bedeutung                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Der Beispiel Grabber wird nach dem ersten Beispiel angehalten. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Nach dem ersten Beispiel verarbeitet der Beispiel Grabber weiterhin Beispiele. Dies ist das Standardverhalten.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um ein einzelnes Beispiel aus dem Datenstrom zu erhalten, wie im folgenden dargestellt:

1.  Nennen **Sie** "*" mit dem Wert " **true**".
2.  Optional können Sie die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle verwenden, um eine Position im Stream zu suchen.
3.  Nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , um das Filter Diagramm auszuführen.
4.  Nennen Sie [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) , um zu warten, bis das Diagramm angehalten wird. Rufen Sie alternativ [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) auf, um Diagramm Ereignisse abzurufen, bis Sie das Ereignis " [**EC \_ Complete**](ec-complete.md) " erhalten.

Nachdem die Stichprobenentnahme angehalten wurde, befindet sich das Filter Diagramm weiterhin in einem laufenden Zustand. Sie können das Diagramm suchen oder anhalten, um ein weiteres Beispiel zu erhalten.

> [!Note]  
> Eine frühere Version der Dokumentation hat besagt, dass das Filter Diagramm beendet wird, nachdem das Beispiel empfangen wurde. Das ist nicht korrekt. Der Stream wird beendet, der Graph verbleibt jedoch im Zustand "wird ausgeführt".

 

Der Beispiel-Grabber implementiert den One-Shot-Modus durch Aufrufen von [**IPin:: EndOfStream für den downstreamfilter**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) und das Zurückgeben von " \_ false" aus der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Beispiel-Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**Isamplegrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




