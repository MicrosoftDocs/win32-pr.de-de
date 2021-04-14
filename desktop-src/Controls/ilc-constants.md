---
title: Abbild Listen-erstellungsflags (shlobj. h)
description: Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt. Dieser Parameter kann eine Kombination der folgenden Werte sein, kann jedoch nur einen der ILC- \_ Farbwerte enthalten. Wird von ImageList \_ Create und IImageList2 Initialize verwendet.
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
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476317"
---
# <a name="image-list-creation-flags"></a>Abbild Listen-Erstellungs Flags

Der Satz von Bitflags, der den Typ der zu erstellenden Bildliste angibt. Dieser Parameter kann eine Kombination der folgenden Werte sein, kann jedoch nur einen der ILC- \_ Farbwerte enthalten. Wird von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) und [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize)verwendet.



| Konstante/Wert                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ Maske**</dt> <dt>0x00000001</dt> </dl>                                     | Verwenden Sie eine Maske. Die Bildliste enthält zwei Bitmaps, von denen eine eine monochrome Bitmap ist, die als Maske verwendet wird. Wenn dieser Wert nicht eingeschlossen ist, enthält die Bildliste nur eine Bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ Farbe**</dt> <dt>0x00000000</dt> </dl>                                  | Verwenden Sie das Standardverhalten, wenn keines der anderen ILC \_ ColorX-Flags angegeben wird. In der Regel ist der Standardwert ILC \_ COLOR4, aber für ältere Anzeigetreiber lautet der Standardwert ILC \_ colorddb.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ Colorddb**</dt> <dt>0x000000FE</dt> </dl>                         | Verwenden Sie eine Geräte abhängige Bitmap.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Verwenden Sie einen 4-Bit-Abschnitt (16-farbig) geräteunabhängige Bitmap (DIB) als Bitmap für die Bildliste.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Verwenden Sie einen 8-Bit-DIB-Abschnitt. Die Farben, die für die Farbtabelle verwendet werden, entsprechen den Farben der halbftone-Palette.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Verwenden Sie einen 16-Bit-DIB-Abschnitt (32/64K-Color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Verwenden Sie einen 24-Bit-DIB-Abschnitt.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Verwenden Sie einen 32-Bit-DIB-Abschnitt.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ Palette**</dt> <dt>0x00000800</dt> </dl>                            | Nicht implementiert.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ Spiegelung**</dt> <dt>0x00002000</dt> </dl>                               | Spiegelung der enthaltenen Symbole, wenn der Prozess gespiegelt wird<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ Peritemmirror**</dt> <dt>0x00008000</dt> </dl>          | Bewirkt, dass der Spiegelungs Code jedes Element Spiegelung, wenn ein Satz von Bildern eingefügt wird, im Vergleich zum gesamten Strip.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ OriginalSize**</dt> <dt>0x00010000 bis</dt> </dl>             | **Windows Vista und höher.** ImageList sollte kleiner als festgelegte Images annehmen und die ursprüngliche Größe basierend auf dem hinzugefügten Image anwenden.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ Highqualityscale**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista und höher.** Reserviert.<br/>                                                                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 





