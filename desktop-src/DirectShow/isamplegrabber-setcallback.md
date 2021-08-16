---
description: Die SetCallback-Methode gibt eine Rückrufmethode zum Aufrufen eingehender Stichproben an.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: ISampleGrabber::SetCallback-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e6d61d60a4664386cded025d2b7bcea82353602c7f7f8c0fb5bc4c53779ae2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817917"
---
# <a name="isamplegrabbersetcallback-method"></a>ISampleGrabber::SetCallback-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die **SetCallback-Methode** gibt eine Rückrufmethode zum Aufrufen eingehender Stichproben an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCallback* 
</dt> <dd>

Zeiger auf eine [**ISampleGrabberCB-Schnittstelle,**](isamplegrabbercb.md) die die Rückrufmethode enthält, oder **NULL** zum Abbrechen des Rückrufs.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Index, der die Rückrufmethode an gibt. Dabei muss es sich um einen der folgenden Werte handeln.



| Wert | Beschreibung                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Der Beispielgrabberfilter ruft die [**ISampleGrabberCB::SampleCB-Methode**](isamplegrabbercb-samplecb.md) auf. Diese Methode empfängt einen [**IMediaSample-Zeiger.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)               |
| 1     | Der Beispielgrabberfilter ruft die [**ISampleGrabberCB::BufferCB-Methode**](isamplegrabbercb-buffercb.md) auf. Diese Methode empfängt einen Zeiger auf den Puffer, der im Medienbeispiel enthalten ist. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der Datenverarbeitungsthread wird blockiert, bis die Rückrufmethode zurückgegeben wird. Wenn der Rückruf nicht schnell zurückkehrt, kann dies die Wiedergabe beeinträchtigen.

Der Filter ruft die Rückruffunktion nicht für Vorabrollbeispiele oder für Beispiele auf, in denen das **dwStreamId-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) etwas anderes als AM \_ STREAM MEDIA \_ ist.

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

 

 




