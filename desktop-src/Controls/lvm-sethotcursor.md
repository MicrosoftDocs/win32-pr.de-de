---
title: LVM_SETHOTCURSOR Meldung (Commctrl.h)
description: Legt den HCURSOR-Wert fest, den das Listenansichtssteuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die heiße Nachverfolgung aktiviert ist.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3407c5d8b53483d3a639fc40959768b3fa8eea0e7b439ab8871d36346b7079d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077250"
---
# <a name="lvm_sethotcursor-message"></a>LVM \_ SETHOTCURSOR-Nachricht

Legt den HCURSOR-Wert fest, den das Listenansichtssteuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die heiße Nachverfolgung aktiviert ist. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) verwenden. Um zu überprüfen, ob hot tracking aktiviert ist, rufen [**Sie SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)auf.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für den festzulegenden Cursor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HCURSOR-Wert zurück, der der vorherige Hotcursor ist.

## <a name="remarks"></a>Hinweise

Ein Listenansichtssteuerelement verwendet die heiße Nachverfolgung und die Auswahl mit dem Mauszeiger, wenn der [**LVS \_ EX \_ TRACKSELECT-Stil**](extended-list-view-styles.md) festgelegt ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

