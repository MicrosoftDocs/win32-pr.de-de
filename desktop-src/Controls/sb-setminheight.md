---
title: SB_SETMINHEIGHT (Commctrl.h)
description: Legt die Mindesthöhe des Zeichnungsbereichs eines Statusfensters fest.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b644067e48312b265d132f7d06d53343c4612b879c3a09b638ebd0a98a7c88a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293730"
---
# <a name="sb_setminheight-message"></a>SB \_ SETMINHEIGHT-Nachricht

Legt die Mindesthöhe des Zeichnungsbereichs eines Statusfensters fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mindesthöhe des Fensters in Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Mindesthöhe ist die Summe *von wParam* und die doppelte Breite des vertikalen Rahmens des Statusfensters in Pixel. Eine Anwendung muss die [**WM \_ SIZE-Nachricht**](/windows/desktop/winmsg/wm-size) an das Statusfenster senden, um das Fenster neu zu zeichnet. Die *Parameter wParam* *und lParam* der **WM \_ SIZE-Meldung** sollten auf 0 (null) festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

