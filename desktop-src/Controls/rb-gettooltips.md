---
title: RB_GETTOOLTIPS (Commctrl.h)
description: Ruft das Handle für ein beliebiges QuickInfo-Steuerelement ab, das dem Rebar-Steuerelement zugeordnet ist.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859934dcdec85d0b160f9076f2a77263a02a187ebf49f8ccbb4af20fc3e82d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540060"
---
# <a name="rb_gettooltips-message"></a>RB \_ GETTOOLTIPS-Nachricht

Ruft das Handle für ein beliebiges QuickInfo-Steuerelement ab, das dem Rebar-Steuerelement zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HWND-Wert** zurück, der das Handle für das QuickInfo-Steuerelement ist, das dem Rebar-Steuerelement zugeordnet ist, oder 0 (null), wenn dem Rebar-Steuerelement kein QuickInfo-Steuerelement zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





