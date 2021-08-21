---
title: TBM_SETTIC (Commctrl.h)
description: Legt einen Teilstrich in einer Trackleiste an der angegebenen logischen Position fest.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f286a2f03e318629a10651d066da5aa6cfe70aa293f242ad7508d0ef4739a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540020"
---
# <a name="tbm_settic-message"></a>TBM \_ SETTIC-Meldung

Legt einen Teilstrich in einer Trackleiste an der angegebenen logischen Position fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Position des Teilstrichs. Dieser Parameter kann ein beliebiger ganzzahliger Wert im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Teilstrich festgelegt ist, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Eine Trackleiste erstellt eigene erste und letzte Teilstriche. Verwenden Sie diese Meldung nicht zum Festlegen der ersten und letzten Teilstriche.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TBM \_ GETPTICS**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GETTIC**](tbm-gettic.md)
</dt> </dl>

 

 





