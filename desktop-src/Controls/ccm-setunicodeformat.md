---
title: CCM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- Windows-Steuerelemente für CCM_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477628"
---
# <a name="ccm_setunicodeformat-message"></a>CCM-Nachricht "*- \_ Code Format"

Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein-Wert, der den Zeichensatz bestimmt, der vom-Steuerelement verwendet wird. Wenn dieser Wert **true** ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert **false** ist, verwendet das Steuerelement ANSI-Zeichen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCM \_ getunicodeformat**](ccm-getunicodeformat.md)
</dt> </dl>

 

 





