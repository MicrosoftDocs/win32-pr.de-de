---
title: RB_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements fest.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Windows-Steuerelemente für RB_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345303"
---
# <a name="rb_setbkcolor-message"></a>RB- \_ SetBkColor-Meldung

Legt die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Standard Hintergrundfarbe darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Standard Hintergrundfarbe darstellt.

## <a name="remarks"></a>Bemerkungen

Die Standard Hintergrundfarbe des Grund leisten-Steuer Elements wird verwendet, um den Hintergrund in einem Grund leisten-Steuerelement und alle Bänder zu zeichnen, die nach dem Senden dieser Nachricht hinzugefügt werden. Die Standard Hintergrundfarbe für ein bestimmtes Band kann überschrieben werden, wenn ein Band hinzugefügt oder geändert wird, indem das Flag rbbim \_ Colors in der Datei **Maske** **festgelegt** und in der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur festgelegt wird.

Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ GetBkColor**](rb-getbkcolor.md)
</dt> </dl>

 

