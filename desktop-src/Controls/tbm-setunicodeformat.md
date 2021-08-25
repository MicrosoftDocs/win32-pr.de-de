---
title: TBM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'TBM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.'
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2c6635f895d8ebd11f8261da553fe59d65574151046f97e489a6d9c6990d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877000"
---
# <a name="tbm_setunicodeformat-message"></a>TBM \_ SETUNICODEFORMAT-Nachricht

Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird. Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.

## <a name="remarks"></a>Hinweise

Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md)
</dt> </dl>

 

 





