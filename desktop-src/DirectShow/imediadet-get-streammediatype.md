---
description: Die methode \_ get StreamMediaType ruft den Medientyp des aktuellen Streams ab. Alle Videostreams werden in VIDEOINFOHEADER-Typen konvertiert, und alle Audiostreams werden in WAVEFORMATEX-Typen konvertiert.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: IMediaDet::get_StreamMediaType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e62f7c7d5a6881647280e17d7ae21c442ae57c21a0c48470e255434007c5db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154182"
---
# <a name="imediadetget_streammediatype-method"></a>IMediaDet::get \_ StreamMediaType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_StreamMediaType` -Methode ruft den Medientyp des aktuellen Streams ab. Alle Videostreams werden in [**VIDEOINFOHEADER-Typen**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) konvertiert, und alle Audiostreams werden in [**WAVEFORMATEX-Typen**](/previous-versions/dd757713(v=vs.85)) konvertiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die mit dem Medientyp gefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und stream fest, indem Sie [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream aufrufen.**](imediadet-put-currentstream.md)

Wenn sich die Medienerkennung im Bitmap-Greifmodus befindet, gibt diese Methode E \_ INVALIDARG zurück. Weitere Informationen finden Sie unter [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 
