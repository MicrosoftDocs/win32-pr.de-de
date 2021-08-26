---
description: Die GetImageSize-Methode ruft Informationen zur Videobildgröße ab.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: CBaseControlVideo.GetImageSize-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a7e0d970e06186ced3800d4b1f4dc4190778834941b69ac17402e2294312b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057060"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>CBaseControlVideo.GetImageSize-Methode

Die `GetImageSize` -Methode ruft Informationen zur Videobildgröße ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Zeiger auf eine [**VIDEOINFOHEADER-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) die ausgefüllt werden soll.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Zeiger auf die Größe des Videopuffers.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Zeiger auf die Rechteckdimensionen des Quellvideos.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte sein, oder andere Werte, die nicht aufgeführt sind.



| Rückgabecode                                                                                  | Beschreibung                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Fehler.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument. Das Datenformat ist nicht kompatibel.<br/>           |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler. Mindestens ein Argument ist **NULL.**<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Erfolg.<br/>                                                       |



 

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ist eine Hilfsfunktion, die zum Erstellen von Speicherbildrenderings von DIB-Bildern verwendet wird. Sie wird von der Basisklassenimplementierung von [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) aufgerufen, wenn ein _NULL-pVideoImage-Parameter_ an diese Memberfunktion übergeben wird.  Daher erstellt diese Memberfunktion eine [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und gibt sie mithilfe der Informationen in *pBufferSize* und *pSourceRect* zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




