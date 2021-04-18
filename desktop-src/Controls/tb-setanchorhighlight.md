---
title: TB_SETANCHORHIGHLIGHT Meldung (kommstrg. h)
description: Legt die Anker Hervorhebungs Einstellung für eine Symbolleiste fest.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Windows-Steuerelemente für TB_SETANCHORHIGHLIGHT Meldung
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341357"
---
# <a name="tb_setanchorhighlight-message"></a>TB-Nachricht "- \_ Abmeldung"

Legt die Anker Hervorhebungs Einstellung für eine Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Boolescher** Wert, der angibt, ob Anker Hervorhebung aktiviert oder deaktiviert ist. Wenn dieser Wert ungleich 0 (null) ist, wird die Anker Markierung aktiviert. Wenn dieser Wert 0 (null) ist, wird die Anker Markierung deaktiviert.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Anker Hervorhebungs Einstellung zurück. Wenn dieser Wert ungleich 0 (null) ist, wurde die Anker Markierung aktiviert. Wenn dieser Wert 0 (null) ist, wurde die Anker Markierung deaktiviert.

## <a name="remarks"></a>Bemerkungen

Die Anker Markierung in einer Symbolleiste bedeutet, dass das letzte markierte Element hervorgehoben bleibt, bis ein anderes Element hervorgehoben wird. Dies tritt auch auf, wenn der Cursor das Symbolleisten-Steuerelement verlässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





