---
title: EM_SETBKGNDCOLOR Meldung (RichEdit. h)
description: Die "em \_ setbkgndcolor"-Meldung legt die Hintergrundfarbe für ein Rich-Edit-Steuerelement fest.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Windows-Steuerelemente für EM_SETBKGNDCOLOR Meldung
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
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859174"
---
# <a name="em_setbkgndcolor-message"></a>EM \_ setbkgndcolor-Meldung

Die " **EM \_ setbkgndcolor** "-Meldung legt die Hintergrundfarbe für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die System Farbe verwendet werden soll. Wenn dieser Parameter ein Wert ungleich 0 (null) ist, wird der Hintergrund auf die Hintergrundsystem Farbe des Fensters festgelegt. Andernfalls wird der Hintergrund auf die angegebene Farbe festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**COLORREF**](/windows/desktop/gdi/colorref) -Struktur, die die Farbe angibt, wenn *wParam* NULL ist. Verwenden Sie zum Generieren eines **COLORREF** das [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) -Makro.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die ursprüngliche Hintergrundfarbe zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

