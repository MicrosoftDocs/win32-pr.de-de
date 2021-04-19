---
description: Die checkstreamstate-Methode bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Cbasestreamcontrol. checkstreamstate-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352916"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>Cbasestreamcontrol. checkstreamstate-Methode

Die- `CheckStreamState` Methode bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.

## <a name="syntax"></a>Syntax


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                       | Beschreibung                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**Stream- \_ verwerfen**</dt> </dl> | Verwerfen Sie dieses Beispiel.<br/> |
| <dl> <dt>**Stream \_ fließt**</dt> </dl>    | Liefern Sie dieses Beispiel.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, wenn Ihre PIN ein Beispiel empfängt. Übermitteln Sie das Beispiel nur dann, wenn der Rückgabewert Stream \_ fließt. Wenn der Rückgabewert Stream- \_ verwerfen ist, verwerfen Sie das Beispiel.

Wenn die PIN Beispiele verwirft, sollte das nächste Beispiel, das es als Diskontinuität bereitstellt, durch Aufrufen der [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode gekennzeichnet werden.

Wenn Ihr Filter die [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) -Schnittstelle implementiert, um zu zählen, wie viele Frames Sie löscht, zählen Sie keinen verworfenen Frame als einen gelöschten Frame.

Wenn der Rückgabewert Stream \_ -verwerfen ist, wird die-Methode blockiert, bis die Verweis Zeit die Startzeit des Beispiels erreicht. Dadurch wird verhindert, dass Ihre PIN die Stichproben zu schnell verwerfen. Wenn der Filter angehalten ist, ist die Wartezeit unendlich, bis der Filter ausgeführt, beendet oder leert. (Filter Zustandsänderungen und Streaming erfolgen in separaten Threads, sodass dies keinen Deadlock verursacht.)

Die **cbasestreamcontrol:: streamcontrolstate** -Enumeration ist wie folgt definiert:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird davon ausgegangen, dass die PIN eine Member-Variable mit dem Namen m \_ flastsampleverworfen verwendet, um Diskontinuitäten nachzuverfolgen.


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




