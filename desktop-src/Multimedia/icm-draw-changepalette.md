---
title: ICM_DRAW_CHANGEPALETTE Meldung (VFW. h)
description: Die ICM \_ Draw \_ changepalette-Meldung benachrichtigt einen renderingtreiber, dass sich die Film Palette ändert. Sie können diese Nachricht explizit oder mithilfe des icdrawchangepalette-Makros senden.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858986"
---
# <a name="icm_draw_changepalette-message"></a>ICM- \_ Meldung zum Zeichnen der \_ changepalette

Die **ICM \_ Draw \_ changepalette** -Meldung benachrichtigt einen renderingtreiber, dass sich die Film Palette ändert. Sie können diese Nachricht explizit oder mithilfe des [**icdrawchangepalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) -Makros senden.


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*
</dt> <dd>

Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das neue Format und die optionale Farbtabelle enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls **false** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung sollte von installierbaren renderhandlern unterstützt werden, die Disb mit einer internen Struktur zeichnen, die eine Palette enthält.

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

 

