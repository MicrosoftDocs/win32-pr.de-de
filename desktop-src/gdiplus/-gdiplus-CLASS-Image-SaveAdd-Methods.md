---
description: In diesem Thema werden die SaveAdd-Methoden der Image-Klasse aufgeführt. Eine vollständige Liste der Methoden für die Image-Klasse finden Sie unter Bildmethoden.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Image.SaveAdd-Methoden (Gdiplusheaders.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b9a18e1c74bf858db8ee3f8877a714338c1ed8b08a87b9e501dcc980bb6f78e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717590"
---
# <a name="imagesaveadd-methods"></a>Image.SaveAdd-Methoden

In diesem Thema werden die SaveAdd-Methoden der [**Image-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aufgeführt. Eine vollständige Liste der Methoden für die **Image-Klasse** finden Sie unter [Bildmethoden](-gdiplus-class-image-methods.md).

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                               | Beschreibung                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaveAdd(EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))                  | Die [**Image::SaveAdd-Methode**](/previous-versions//ms535408(v=vs.85)) fügt einer Datei oder einem Stream, die in einem vorherigen Aufruf der **Save-Methode** angegeben wurde, einen Frame hinzu. Mit dieser Methode speichern Sie ausgewählte Rahmen eines Bilds mit mehreren Rahmen in einem anderen Bild mit mehreren Rahmen.<br/> |
| [**SaveAdd(Image \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) | Die [**Image::SaveAdd-Methode**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) fügt einer Datei oder einem Stream, die in einem vorherigen Aufruf der **Save-Methode** angegeben wurde, einen Frame hinzu.<br/>                                                                                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Xp, Windows 2000 Professional \[ Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                            |
| Produkt<br/>                  | GDI+ 1.0<br/>                                                                                             |
| Header<br/>                   | <dl> <dt>Gdiplusheaders.h (einschließlich Gdiplus.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Gdiplus.lib</dt> </dl>                          |



 

 
