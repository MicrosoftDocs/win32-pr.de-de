---
title: RB_SETTEXTCOLOR (Commctrl.h)
description: Legt die Standardtextfarbe eines Rebar-Steuerelements fest.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR von Windows Steuerelementen
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
ms.openlocfilehash: 88458f5a131250dbb261040bf26689356c1ba5446db854839ded05ff287a14ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078614"
---
# <a name="rb_settextcolor-message"></a>RB \_ SETTEXTCOLOR-Meldung

Legt die Standardtextfarbe eines Rebar-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die neue Standardtextfarbe darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der die vorherige Standardtextfarbe darstellt.

## <a name="remarks"></a>Hinweise

Die Standardtextfarbe des Rebar-Steuerelements wird verwendet, um den Text in einem Rebar-Steuerelement und alle Bänder zu zeichnen, die nach dem Senden dieser Nachricht hinzugefügt werden. Die Standardtextfarbe für ein bestimmtes Band kann überschrieben werden, wenn ein Band hinzugefügt oder geändert wird, indem das Flag RBBIM \_ COLORS in **fMask** und **clrBack** in der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)
</dt> </dl>

 

