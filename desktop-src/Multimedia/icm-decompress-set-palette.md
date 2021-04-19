---
title: ICM_DECOMPRESS_SET_PALETTE Meldung (VFW. h)
description: Die ICM \_ Decompress \_ Set \_ Palette-Meldung gibt eine Palette für einen Video Dekomprimierungs Treiber an, der verwendet werden soll, wenn er zu einem Format dekomprimiert, das eine Palette verwendet. Sie können diese Nachricht explizit oder mithilfe des icdecompresssetpalette-Makros senden.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345502"
---
# <a name="icm_decompress_set_palette-message"></a>ICM- \_ Dekomprimierungs Meldung zum Dekomprimieren der \_ \_ Palette

Die **ICM \_ Decompress \_ Set \_ Palette** -Meldung gibt eine Palette für einen Video Dekomprimierungs Treiber an, der verwendet werden soll, wenn er zu einem Format dekomprimiert, das eine Palette verwendet. Sie können diese Nachricht explizit oder mithilfe des [**icdecompresssetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) -Makros senden.


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbipalette*
</dt> <dd>

Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, deren Farbtabelle die Farben enthält, die nach Möglichkeit verwendet werden sollen. Sie können NULL angeben, um den Standardsatz von Ausgabe Farben zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Debug-Treiber Bilder mithilfe des Satzes von Farben, die in der Palette angeordnet sind, genau in die vorgeschlagene Palette decokomprimieren kann. Gibt ICERR zurück, \_ wird andernfalls nicht unterstützt.

## <a name="remarks"></a>Bemerkungen

Diese Meldung sollte sich nicht auf die bereits ausgeführte Dekomprimierung auswirken. Stattdessen sollten mit dieser Nachricht über gegebene Farben als Reaktion auf zukünftiges [**ICM \_ Decompress get- \_ \_ Format**](icm-decompress-get-format.md) und [**ICM \_ Decompress \_ get \_ Palette**](icm-decompress-get-palette.md) Messages zurückgegeben werden. Farben werden in einer zukünftigen [**ICM- \_ Dekomprimierungs \_ Begin**](icm-decompress-begin.md) -Meldung an den dekomprimierungstreiber zurückgesendet.

Diese Meldung wird hauptsächlich verwendet, wenn ein Treiber Bilder auf den Bildschirm dekomprimiert und eine andere Anwendung, die eine Palette verwendet, im Vordergrund steht, wodurch der dekomprimierungstreiber an einen anderen Satz von Farben angepasst wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

