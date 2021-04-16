---
title: RB_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Standard Textfarbe eines Grund leisten-Steuer Elements fest.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Windows-Steuerelemente für RB_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477859"
---
# <a name="rb_settextcolor-message"></a>RB \_ SetTextColor-Meldung

Legt die Standard Textfarbe eines Grund leisten-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Standard Textfarbe darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Standard Textfarbe darstellt.

## <a name="remarks"></a>Bemerkungen

Die Standard Textfarbe des Grund leisten-Steuer Elements wird verwendet, um den Text in einem Grund leisten-Steuerelement und alle Bänder zu zeichnen, die nach dem Senden dieser Nachricht hinzugefügt werden. Die Standard Textfarbe für ein bestimmtes Band kann überschrieben werden, wenn ein Band hinzugefügt oder geändert wird, indem das Flag rbbim \_ Colors in der Datei **Maske** festgelegt und **clrback** in der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ gettextcolor**](rb-gettextcolor.md)
</dt> </dl>

 

