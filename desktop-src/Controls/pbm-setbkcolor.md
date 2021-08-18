---
title: PBM_SETBKCOLOR Meldung (Commctrl.h)
description: Legt die Hintergrundfarbe in der Statusleiste fest.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54bdee330aba5a4ff96fc5b26fa7f99553ff8331dd8822fcd350fbae5813c813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986180"
---
# <a name="pbm_setbkcolor-message"></a>PBM \_ SETBKCOLOR-Nachricht

Legt die Hintergrundfarbe in der Statusleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF-Wert,** der die neue Hintergrundfarbe angibt. Geben Sie den CLR \_ DEFAULT-Wert an, damit die Statusanzeige die Standardhintergrundfarbe verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hintergrundfarbe oder CLR \_ DEFAULT zurück, wenn die Hintergrundfarbe die Standardfarbe ist.

## <a name="remarks"></a>Hinweise

Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





