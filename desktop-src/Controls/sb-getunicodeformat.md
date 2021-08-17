---
title: SB_GETUNICODEFORMAT Meldung (Commctrl.h)
description: 'SB_GETUNICODEFORMAT Meldung: Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.'
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6a00725b5c161e6b2a85aae9e21436e4826619b0336ffedf7eaa307c285ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409170"
---
# <a name="sb_getunicodeformat-message"></a>SB \_ GETUNICODEFORMAT-Nachricht

Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Unicode-Formatflag für das Steuerelement zurück. Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.

## <a name="remarks"></a>Hinweise

Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md)
</dt> </dl>

 

 





