---
title: LVM_SETHOTCURSOR Meldung (kommstrg. h)
description: Legt den hcursor-Wert fest, den das Listenansicht-Steuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die Hot-Überwachung aktiviert ist.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Windows-Steuerelemente für LVM_SETHOTCURSOR Meldung
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
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739945"
---
# <a name="lvm_sethotcursor-message"></a>LVM- \_ messagecursor-Nachricht

Legt den hcursor-Wert fest, den das Listenansicht-Steuerelement verwendet, wenn sich der Zeiger über einem Element befindet, während die Hot-Überwachung aktiviert ist. Sie können diese Nachricht explizit senden oder das [**ListView- \_ prätcursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) -Makro verwenden. Um zu überprüfen, ob Hot Tracking aktiviert ist, aufrufen Sie [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für den Cursor, der festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen hcursor-Wert zurück, der der vorherige Hot-Cursor ist.

## <a name="remarks"></a>Bemerkungen

Ein Listenansicht-Steuerelement verwendet die Hot-Tracking-und Hover-Auswahl, wenn der [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md) -Stil festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

