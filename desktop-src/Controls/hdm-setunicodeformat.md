---
title: HDM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'HDM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- HDM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32ffa5f7f90ab266c52c67899dbff3be0d51123
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085958"
---
# <a name="hdm_setunicodeformat-message"></a>HDM \_ SETUNICODEFORMAT-Nachricht

Legt das UNICODE-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. Sie können diese Nachricht explizit senden oder das [**\_ HeadersetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichensatz, der vom -Steuerelement verwendet wird. Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**HDM \_ GETUNICODEFORMAT**](hdm-getunicodeformat.md)
</dt> </dl>

 

 





