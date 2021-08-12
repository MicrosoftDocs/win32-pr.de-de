---
title: LVM_SETITEMTEXT (Commctrl.h)
description: Ändert den Text eines Listenansichtselements oder Unterelements. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetItemText-Makros senden.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT message Windows Controls
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14eb5ddcff18a84f93febb22ef6661d8871df9b5578cc79f071b6e51b557c87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670873"
---
# <a name="lvm_setitemtext-message"></a>LVM \_ SETITEMTEXT-Nachricht

Ändert den Text eines Listenansichtselements oder Unterelements. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetItemText-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Listenansichtselements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Das **iSubItem-Element** ist der Index des Unterelements, oder es kann 0 (null) sein, um die Elementbezeichnung zu setzen. Das **pszText-Member** ist die Adresse einer auf NULL beendeten Zeichenfolge, die den neuen Text enthält. kann auch NULL **sein.** Der **pszText-Member** kann auch LPSTR TEXTCALLBACK sein, um ein Rückrufelement anzugeben, für das das übergeordnete Fenster \_ den Text speichert. In diesem Fall sendet das Listenansicht-Steuerelement dem übergeordneten Element einen [**LVN GETDISPINFO-Benachrichtigungscode, \_**](lvn-getdispinfo.md) wenn der Text benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie diese Nachricht explizit senden, wird **TRUE** zurückgegeben, wenn sie erfolgreich war, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) und **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





