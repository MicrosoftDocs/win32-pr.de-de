---
title: PBM_SETBARCOLOR Meldung (kommstrg. h)
description: Legt die Farbe der Statusanzeige Leiste im Statusanzeige-Steuerelement fest.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Windows-Steuerelemente für PBM_SETBARCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518287"
---
# <a name="pbm_setbarcolor-message"></a>PBM- \_ setbarcolor-Meldung

Legt die Farbe der Statusanzeige Leiste im Statusanzeige-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Der **COLORREF** -Wert, der die neue Statusanzeige leisten Farbe angibt. Wenn Sie den CLR- \_ Standardwert angeben, wird in der Statusleiste die standardmäßige Statusanzeige leisten Farbe verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Status Indikator leisten Farbe oder CLR-Standardwert zurück, \_ Wenn die Statusanzeige leisten Farbe die Standardfarbe ist.

## <a name="remarks"></a>Bemerkungen

Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





