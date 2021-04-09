---
title: TBM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- Windows-Steuerelemente für TBM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9fafad2504e51a65b879e58298c5cd06f1f345
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858909"
---
# <a name="tbm_getunicodeformat-message"></a>TBM \_ getunicodeformat-Meldung

Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Unicode-formatflag für das-Steuerelement zurück. Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.

## <a name="remarks"></a>Bemerkungen

Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM- \_ Code Format**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





