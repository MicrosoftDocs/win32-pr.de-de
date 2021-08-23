---
title: TB_SETPARENT (Commctrl.h)
description: Legt das Fenster fest, an das das Symbolleisten-Steuerelement Benachrichtigungsmeldungen sendet.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT von Windows-Steuerelementen
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
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078144"
---
# <a name="tb_setparent-message"></a>TB \_ SETPARENT-Nachricht

Legt das Fenster fest, an das das Symbolleisten-Steuerelement Benachrichtigungsmeldungen sendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Fenster zum Empfangen von Benachrichtigungsmeldungen.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das vorherige Benachrichtigungsfenster oder **NULL,** wenn es kein vorheriges Benachrichtigungsfenster gibt.

## <a name="remarks"></a>Hinweise

Die **TB \_ SETPARENT-Meldung** ändert nicht das übergeordnete Fenster, das beim Erstellen des Steuerelements angegeben wurde. Durch aufrufen [**der GetParent-Funktion**](/windows/desktop/api/winuser/nf-winuser-getparent) für ein Symbolleisten-Steuerelement wird das eigentliche übergeordnete Fenster und nicht das in **TB \_ SETPARENT** angegebene Fenster zurückgeben. Um das übergeordnete Fenster des Steuerelements zu ändern, rufen Sie die [**SetParent-Funktion**](/windows/desktop/api/winuser/nf-winuser-setparent) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

