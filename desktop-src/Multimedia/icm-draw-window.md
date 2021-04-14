---
title: ICM_DRAW_WINDOW Meldung (VFW. h)
description: Die ICM- \_ Meldung zum Zeichnen des \_ Fensters benachrichtigt einen renderingtreiber, dass das für die ICM Draw-BEGIN-Meldung angegebene Fenster \_ \_ neu gezeichnet werden muss.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476242"
---
# <a name="icm_draw_window-message"></a>ICM- \_ Zeichnungs \_ Fenster Meldung

Die **ICM-Meldung zum \_ Zeichnen des \_ Fensters** benachrichtigt einen renderingtreiber, dass das für die [**ICM \_ Draw- \_ Begin**](icm-draw-begin.md) -Meldung angegebene Fenster neu gezeichnet werden muss. Das Fenster wurde verschoben oder vorübergehend verdeckt. Sie können diese Nachricht explizit oder mithilfe des [**icdrawwindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) -Makros senden.


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Zeiger auf das Ziel Rechteck in Bildschirm Koordinaten. Wenn dieser Parameter auf ein leeres Rechteck zeigt, sollte das Zeichnen deaktiviert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird von Hardware unterstützt, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.

Videoüberlagerungs Treiber verwenden diese Nachricht, um zu zeichnen, wenn das Fenster verdeckt oder verschoben wird. Wenn ein für den [**ICM- \_ Zeichnen- \_ Anfang**](icm-draw-begin.md) angegebener Fenster vollständig von anderen Fenstern ausgeblendet wird, ist das Ziel Rechteck leer. Treiber sollten Video Überlagerungs Hardware deaktivieren, wenn diese Bedingung auftritt.

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

 

 





