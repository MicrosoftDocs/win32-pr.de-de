---
title: TB_SETHOTITEM2 Nachricht (Commctrl.h)
description: 'TB_SETHOTITEM2 Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104138"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2-Nachricht

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements, das heiß gemacht wird. Wenn dieser Wert -1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Eine Kombination von HICF \_ xxx-Flags. Siehe <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des vorherigen heißen Elements oder -1 zurück, wenn kein heißes Element vorhanden war.

## <a name="remarks"></a>Bemerkungen

Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht über den [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





