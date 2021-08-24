---
title: SB_SETBKCOLOR Meldung (Commctrl.h)
description: Legt die Hintergrundfarbe in einer Statusleiste fest.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637080"
---
# <a name="sb_setbkcolor-message"></a>SB \_ SETBKCOLOR-Nachricht

Legt die Hintergrundfarbe in einer Statusleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die neue Hintergrundfarbe angibt. Geben Sie den CLR \_ DEFAULT-Wert an, damit die Statusleiste die Standardhintergrundfarbe verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hintergrundfarbe oder CLR \_ DEFAULT zurück, wenn die Hintergrundfarbe die Standardfarbe ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

