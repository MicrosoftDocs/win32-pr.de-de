---
title: EM_SETBKGNDCOLOR (Richedit.h)
description: Die EM \_ SETBKGNDCOLOR-Meldung legt die Hintergrundfarbe für ein umfangreiches Bearbeitungssteuer steuerelement fest.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412654"
---
# <a name="em_setbkgndcolor-message"></a>EM \_ SETBKGNDCOLOR-Meldung

Die **EM \_ SETBKGNDCOLOR-Meldung** legt die Hintergrundfarbe für ein umfangreiches Bearbeitungssteuer steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Systemfarbe verwendet werden soll. Wenn dieser Parameter ein Wert ungleich 0 (null) ist, wird der Hintergrund auf die Hintergrundsystemfarbe des Fensters festgelegt. Andernfalls wird der Hintergrund auf die angegebene Farbe festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**COLORREF-Struktur,**](/windows/desktop/gdi/colorref) die die Farbe an gibt, *wenn wParam* 0 (null) ist. Verwenden Sie das **RGB-Makro,** um ein [**COLORREF-Element zu**](/windows/desktop/api/wingdi/nf-wingdi-rgb) generieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die ursprüngliche Hintergrundfarbe zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

