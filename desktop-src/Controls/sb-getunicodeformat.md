---
title: SB_GETUNICODEFORMAT (Commctrl.h)
description: 'SB_GETUNICODEFORMAT Meldung: Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.'
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085898"
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

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md)
</dt> </dl>

 

 





