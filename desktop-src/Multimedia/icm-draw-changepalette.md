---
title: ICM_DRAW_CHANGEPALETTE Nachricht (Vfw.h)
description: Die ICM \_ DRAW \_ CHANGEPALETTE-Nachricht benachrichtigt einen Renderingtreiber, dass sich die Filmpalette ändert. Sie können diese Nachricht explizit oder mithilfe des ICDrawChangePalette-Makros senden.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE nachricht Windows Multimedia
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
ms.openlocfilehash: e936c7dce397910ef70a80e2efa7f3e031ab8a61b8f59fece158d5c28e9e1270
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987596"
---
# <a name="icm_draw_changepalette-message"></a>\_ICM DRAW \_ CHANGEPALETTE-Meldung

Die **ICM \_ DRAW \_ CHANGEPALETTE-Nachricht** benachrichtigt einen Renderingtreiber, dass sich die Filmpalette ändert. Sie können diese Nachricht explizit oder mithilfe des [**ICDrawChangePalette-Makros**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) senden.


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) die das neue Format und die optionale Farbtabelle enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Meldung sollte von installierbaren Renderinghandlern unterstützt werden, die DIBs mit einer internen Struktur zeichnen, die eine Palette enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

