---
title: TB_SETPARENT Meldung (kommstrg. h)
description: Legt das Fenster fest, in das das Symbolleisten-Steuerelement Benachrichtigungs Meldungen sendet.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- Windows-Steuerelemente für TB_SETPARENT Meldung
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859205"
---
# <a name="tb_setparent-message"></a>TB- \_ SetParent-Nachricht

Legt das Fenster fest, in das das Symbolleisten-Steuerelement Benachrichtigungs Meldungen sendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Fenster, um Benachrichtigungs Meldungen zu empfangen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das vorherige Benachrichtigungsfenster, oder **null** , wenn kein vorheriges Benachrichtigungsfenster vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Die **TB- \_ SetParent** -Nachricht ändert das übergeordnete Fenster nicht, das beim Erstellen des Steuer Elements angegeben wurde. Wenn Sie die [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) -Funktion für ein ToolBar-Steuerelement aufrufen, wird das tatsächliche übergeordnete Fenster zurückgegeben, nicht das in **TB \_ SetParent** angegebene Fenster. Um das übergeordnete Fenster des Steuer Elements zu ändern, müssen Sie die [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

