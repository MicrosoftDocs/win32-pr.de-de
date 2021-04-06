---
title: PBM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe in der Statusanzeige fest.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Windows-Steuerelemente für PBM_SETBKCOLOR Meldung
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
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742537"
---
# <a name="pbm_setbkcolor-message"></a>PBM- \_ SetBkColor-Meldung

Legt die Hintergrundfarbe in der Statusanzeige fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** -Wert, der die neue Hintergrundfarbe angibt. Geben Sie den CLR- \_ Standardwert an, damit die Statusanzeige Ihre Standard Hintergrundfarbe verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Hintergrundfarbe bzw. CLR-Standardwert zurück, \_ Wenn die Hintergrundfarbe die Standardfarbe ist.

## <a name="remarks"></a>Bemerkungen

Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





