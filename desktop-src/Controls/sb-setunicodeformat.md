---
title: SB_SETUNICODEFORMAT (Commctrl.h)
description: 'SB_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.'
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085888"
---
# <a name="sb_setunicodeformat-message"></a>SB \_ SETUNICODEFORMAT-Nachricht

Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird. Wenn dieser Wert **TRUE ist,** verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert **FALSE ist,** verwendet das Steuerelement ANSI-Zeichen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md)
</dt> </dl>

 

 





