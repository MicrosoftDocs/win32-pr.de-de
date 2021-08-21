---
title: HKM_GETHOTKEY (Commctrl.h)
description: Ruft den Virtuellen Schlüsselcode und die Modifiziererflags eines heißen Schlüssels aus einem Hot Key-Steuerelement ab.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bfbad1eb5e9a6679a1b3e419a0877e61cd90247ef0cf91b0a30c655f755a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672268"
---
# <a name="hkm_gethotkey-message"></a>HKM \_ GETHOTKEY-Nachricht

Ruft den Virtuellen Schlüsselcode und die Modifiziererflags eines heißen Schlüssels aus einem Hot Key-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Virtuellen Schlüsselcode und modifiziererflags zurück. Der [**LOBYTE-Wert**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode des heißen Schlüssels. Der [**HIBYTE-Wert**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) von **LOWORD** ist der Schlüsselmodifizierer, der die Schlüssel angibt, die eine Hot Key-Kombination definieren. Die Modifiziererflags können eine Kombination der folgenden Werte sein.



| Wert            | Bedeutung      |
|------------------|--------------|
| HOTKEYF \_ ALT     | ALT-TASTE      |
| HOTKEYF-STEUERELEMENT \_ | STEUERTASTE  |
| HOTKEYF \_ EXT     | Erweiterter Schlüssel |
| HOTKEYF \_ SHIFT   | Umschalttaste    |



 

## <a name="remarks"></a>Hinweise

Der von dieser Nachricht zurückgegebene 16-Bit-Wert kann als *wParam-Parameter* in der [**WM \_ SETHOTKEY-Nachricht verwendet**](/windows/desktop/inputdev/wm-sethotkey) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

