---
title: TB_SETHOTITEM (Commctrl.h)
description: 'TB_SETHOTITEM Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM meldungssteuerelemente Windows
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
ms.openlocfilehash: a48de58e07d877d999c2d0388bf32845fce349511da563c3a6b1fa9f9c7b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318840"
---
# <a name="tb_sethotitem-message"></a>TB \_ SETHOTITEM-Nachricht

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements, das als hot -Element verwendet wird. Wenn dieser Wert -1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des vorherigen heißen Elements zurück, oder -1, wenn kein heißes Element vorkommt.

## <a name="remarks"></a>Hinweise

Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht das [**TBSTYLE \_ FLAT-Format**](toolbar-control-and-button-styles.md) haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





