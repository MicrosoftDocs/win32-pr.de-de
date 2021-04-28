---
title: TB_SETHOTITEM (Commctrl.h)
description: 'TB_SETHOTITEM Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104178"
---
# <a name="tb_sethotitem-message"></a>TB \_ SETHOTITEM-Nachricht

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements, das als "Hot" (Heiß) verwendet wird. Wenn dieser Wert -1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des vorherigen heißen Elements zurück, oder -1, wenn kein heißes Element vorkommt.

## <a name="remarks"></a>Bemerkungen

Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht das [**TBSTYLE \_ FLAT-Format**](toolbar-control-and-button-styles.md) haben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





