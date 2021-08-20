---
title: LVM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'LVM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- LVM_SETUNICODEFORMAT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9830cd2f5e0ee43c4ed2cd331b15e59727643c03c4841f0e043078de85802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830681"
---
# <a name="lvm_setunicodeformat-message"></a>LVM \_ SETUNICODEFORMAT-Nachricht

Legt das UNICODE-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) verwenden.

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

[**LVM \_ GETUNICODEFORMAT**](lvm-getunicodeformat.md)
</dt> </dl>

 

 





