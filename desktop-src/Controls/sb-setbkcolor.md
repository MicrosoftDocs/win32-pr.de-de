---
title: SB_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe in einer Statusleiste fest.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Windows-Steuerelemente für SB_SETBKCOLOR Meldung
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
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392115"
---
# <a name="sb_setbkcolor-message"></a>SB- \_ SetBkColor-Nachricht

Legt die Hintergrundfarbe in einer Statusleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Hintergrundfarbe angibt. Geben Sie den CLR- \_ Standardwert an, damit die Statusleiste die Standard Hintergrundfarbe verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hintergrundfarbe bzw. CLR-Standardwert zurück, \_ Wenn die Hintergrundfarbe die Standardfarbe ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

