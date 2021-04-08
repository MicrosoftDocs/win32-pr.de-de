---
title: SB_SETMINHEIGHT Meldung (kommstrg. h)
description: Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Windows-Steuerelemente für SB_SETMINHEIGHT Meldung
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
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956885"
---
# <a name="sb_setminheight-message"></a>SB- \_ setMinHeight-Nachricht

Legt die Mindesthöhe für den Zeichnungs Bereich eines Status Fensters fest.

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

## <a name="remarks"></a>Bemerkungen

Die Mindesthöhe ist die Summe von *wParam* und die doppelte Breite des vertikalen Rahmens des Status Fensters in Pixel. Eine Anwendung muss die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht an das Statusfenster senden, um das Fenster neu zu zeichnen. Der *wParam* -Parameter und der *LPARAM* -Parameter der **WM- \_ Größen** Nachricht sollten auf 0 (null) festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

