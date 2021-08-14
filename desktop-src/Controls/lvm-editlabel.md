---
title: LVM_EDITLABEL Nachricht (Commctrl.h)
description: Beginnt die direkte Bearbeitung des Texts des angegebenen Listenansichtselements. Die Nachricht wählt implizit das angegebene Element aus und konzentriert es. Sie können diese Nachricht explizit oder mithilfe des ListView \_ EditLabel-Makros senden.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411844"
---
# <a name="lvm_editlabel-message"></a>LVM \_ EDITLABEL-Nachricht

Beginnt die direkte Bearbeitung des Texts des angegebenen Listenansichtselements. Die Nachricht wählt implizit das angegebene Element aus und konzentriert es. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ EditLabel-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listenansichtselements. Um die Bearbeitung abzubrechen, legen Sie den Index auf -1 fest.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungssteuerelement zurück, das bei Erfolg zum Bearbeiten des Elementtexts verwendet wird, oder andernfalls **NULL.**

## <a name="remarks"></a>Hinweise

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungssteuerelement zerstört, und das Handle ist nicht mehr gültig. Sie können das Bearbeitungssteuerelement untergliedern, sollten es jedoch nicht zerstören.

Das Steuerelement muss den Fokus haben, bevor Sie diese Nachricht an das Steuerelement senden. Der Fokus kann mithilfe der [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) festgelegt werden.

Wenn *wParam* -1 ist, wird ein [LVN \_ ENDLABELEDIT-Benachrichtigungscode](lvn-endlabeledit.md) gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ EDITLABELW** (Unicode) und **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

