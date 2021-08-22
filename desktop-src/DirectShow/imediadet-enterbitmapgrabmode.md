---
description: Die EnterBitmapGrabMode-Methode schaltet die Medienerkennung in den Bitmapgrabbermodus um und sucht den Filtergraphen zu einer angegebenen Zeit.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: IMediaDet::EnterBitmapGrabMode-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952619"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>IMediaDet::EnterBitmapGrabMode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `EnterBitmapGrabMode` -Methode schaltet die Medienerkennung in den Bitmapgrabbermodus um und sucht das Filterdiagramm zu einer angegebenen Zeit.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StreamTime* 
</dt> <dd>

Die Zeit in Sekunden, nach der das Diagramm sucht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                             | Beschreibung                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Ungültiges Argument.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Die Quelldatei verfügt nicht über einen Videostream.<br/> |
| <dl> <dt>**VFW \_ E \_ TIME \_ EXPIRED**</dt> </dl>    | Time out des Seek-Befehls.<br/>                       |



 

## <a name="remarks"></a>Hinweise

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und den Stream fest, indem [**Sie IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md)aufrufen.

Diese Methode fügt den [**Sample Grabber-Filter**](sample-grabber-filter.md) in das Filterdiagramm ein. Anschließend können Sie [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) aufrufen, um einen Zeiger auf die [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) abzurufen. Sobald die Medienerkennung in den Bitmapgrabbermodus wechselt, funktionieren die verschiedenen Informationsmethoden in **IMediaDet** nicht mehr.

Die [**IMediaDet::GetBitmapBits-**](imediadet-getbitmapbits.md) oder [**IMediaDet::WriteBitmapBits-Methoden**](imediadet-writebitmapbits.md) versetzen die Medienerkennung auch in den Bitmapgrabbermodus.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




