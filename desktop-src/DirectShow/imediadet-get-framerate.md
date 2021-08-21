---
description: Die get \_ FrameRate-Methode ruft die Framerate des aktuellen Streams ab. Der Stream muss ein Videostream sein.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: IMediaDet::get_FrameRate-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a22be2caf5a66447c9c772861918f1a5dcfe7bc2c81bfdba4f1fefb59f89565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154426"
---
# <a name="imediadetget_framerate-method"></a>IMediaDet::get \_ FrameRate-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_FrameRate` -Methode ruft die Framerate des aktuellen Streams ab. Der Stream muss ein Videostream sein.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt die Bildfrequenz in Frames pro Sekunde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Der Videoformatheader gibt keine Bildfrequenz an.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Ungültiges Argument.<br/>                                  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>               |  NULL-Zeigerargument.<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Ungültiger Medientyp.<br/>                                |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann die Bildfrequenz nicht aus einer ASF-Datei abrufen.

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

 

 




