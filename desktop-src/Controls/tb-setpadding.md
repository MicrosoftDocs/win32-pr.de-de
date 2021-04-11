---
title: TB_SETPADDING Meldung (kommstrg. h)
description: Legt die Auffüll Zeichen für ein Symbolleisten-Steuerelement fest.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Windows-Steuerelemente für TB_SETPADDING Meldung
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105752"
---
# <a name="tb_setpadding-message"></a>TB- \_ setPadding-Meldung

Legt die Auffüll Zeichen für ein Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den horizontalen Abstand in Pixel an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den vertikalen Abstand in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der den vorherigen horizontalen Auffüllung im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und den vorherigen vertikalen Abstand im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in Pixel enthält.

## <a name="remarks"></a>Bemerkungen

Die Auffüll Werte werden verwendet, um einen leeren Bereich zwischen dem Rand der Schaltfläche und dem Bild und/oder Text der Schaltfläche zu erstellen. Wo und wie groß die Auffüll Zeichen tatsächlich angewendet werden, hängt vom Typ der Schaltfläche und davon ab, ob Sie über ein Bild verfügt. Der horizontale Abstand wird auf die Rechte und linke Seite der Schaltfläche angewendet, und die vertikale Auffüll Fläche wird auf den oberen und unteren Rand der Schaltfläche angewendet. Auffüll Zeichen werden nur auf Schaltflächen angewendet, die den tbstyle-Stil für die [**\_ Automatische Größe**](toolbar-control-and-button-styles.md) aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ getpadding**](tb-getpadding.md)
</dt> </dl>

 

