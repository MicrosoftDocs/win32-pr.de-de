---
title: TB_SETPADDING-Nachricht (Commctrl.h)
description: Legt die Auffüllung für ein Symbolleistensteuerelement fest.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078164"
---
# <a name="tb_setpadding-message"></a>TB \_ SETPADDING-Nachricht

Legt die Auffüllung für ein Symbolleistensteuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die horizontale Auffüllung in Pixel an. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die vertikale Auffüllung in Pixel an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der die vorherige horizontale Auffüllung in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und die vorherige vertikale Auffüllung im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in Pixel enthält.

## <a name="remarks"></a>Hinweise

Die Auffüllwerte werden verwendet, um einen leeren Bereich zwischen dem Rand der Schaltfläche und dem Bild und/oder Text der Schaltfläche zu erstellen. Wo und wie viel Auffüllung tatsächlich angewendet wird, hängt vom Typ der Schaltfläche und davon ab, ob sie über ein Bild verfügt. Die horizontale Auffüllung wird sowohl auf die rechte als auch auf die linke Seite der Schaltfläche angewendet, und die vertikale Auffüllung wird sowohl auf den oberen als auch auf den unteren Rand der Schaltfläche angewendet. Die Auffüllung wird nur auf Schaltflächen angewendet, die den [**TBSTYLE \_ AUTOIZE-Stil**](toolbar-control-and-button-styles.md) aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

