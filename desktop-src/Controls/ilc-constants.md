---
title: ImageListenerstellungsflags (Shlobj.h)
description: Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt. Dieser Parameter kann eine Kombination der folgenden Werte sein, kann aber nur einen der ILC \_ COLOR-Werte enthalten. Wird von ImageList \_ Create und IImageList2 Initialize verwendet.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1197604750e5da9248200b2dbcf37e53611d83842a401aafc3d2ded70c9179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958689"
---
# <a name="image-list-creation-flags"></a>ImageListenerstellungsflags

Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt. Dieser Parameter kann eine Kombination der folgenden Werte sein, kann aber nur einen der ILC \_ COLOR-Werte enthalten. Wird von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) und [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize)verwendet.



| Konstante/Wert                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ MASK**</dt> <dt>0x00000001</dt> </dl>                                     | Verwenden Sie eine Maske. Die Bildliste enthält zwei Bitmaps, von denen eine eine monocolore Bitmap ist, die als Maske verwendet wird. Wenn dieser Wert nicht enthalten ist, enthält die Bildliste nur eine Bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ COLOR**</dt> <dt>0x00000000</dt> </dl>                                  | Verwenden Sie das Standardverhalten, wenn keins der anderen \_ ILC-COLORx-Flags angegeben ist. In der Regel ist der Standardwert ILC \_ COLOR4, aber für ältere Anzeigetreiber ist der Standardwert ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ COLORDDB-0x000000FE**</dt> <dt></dt> </dl>                         | Verwenden Sie eine geräteabhängige Bitmap.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4-0x00000004**</dt> <dt></dt> </dl>                               | Verwenden Sie einen Geräteunabhängigen 4-Bit-Bitmapabschnitt (DIB) mit 16 Farben als Bitmap für die Bildliste.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8-0x00000008**</dt> <dt></dt> </dl>                               | Verwenden Sie einen 8-Bit-DIB-Abschnitt. Die für die Farbtabelle verwendeten Farben sind die gleichen Farben wie die Halbtonpalette.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Verwenden Sie einen 16-Bit-DIB-Abschnitt (32/64k-Color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Verwenden Sie einen 24-Bit-DIB-Abschnitt.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Verwenden Sie einen 32-Bit-DIB-Abschnitt.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ PALETTE**</dt> <dt>0x00000800</dt> </dl>                            | Nicht implementiert.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ MIRROR**</dt> <dt>0x00002000</dt> </dl>                               | Spiegeln der enthaltenen Symbole, wenn der Prozess gespiegelt wird<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Bewirkt, dass der Spiegelungscode jedes Element beim Einfügen einer Gruppe von Bildern im Vergleich zum gesamten Strip spiegelt.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista und höher.** Imagelist sollte kleiner als festgelegte Images sein und die ursprüngliche Größe basierend auf dem hinzugefügten Bild anwenden.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista und höher.** Reserviert.<br/>                                                                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 





