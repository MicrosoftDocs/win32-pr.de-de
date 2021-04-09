---
title: EM_CANPASTE Meldung (RichEdit. h)
description: Bestimmt, ob ein Rich Edit-Steuerelement ein angegebenes Zwischenablage Format einfügen kann.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Windows-Steuerelemente für EM_CANPASTE Meldung
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040769"
---
# <a name="em_canpaste-message"></a>EM \_ CanPaste-Nachricht

Bestimmt, ob ein Rich Edit-Steuerelement ein angegebenes Zwischenablage Format einfügen kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die zu Try- [Zwischenablage Formate](/windows/desktop/dataxchg/clipboard-formats) an. Wenn Sie ein beliebiges Format in der Zwischenablage ausprobieren möchten, legen Sie diesen Parameter auf NULL fest.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Zwischenablage Format eingefügt werden kann, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn das Zwischenablage Format nicht eingefügt werden kann, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

