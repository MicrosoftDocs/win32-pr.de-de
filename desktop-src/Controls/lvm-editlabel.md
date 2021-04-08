---
title: LVM_EDITLABEL Meldung (kommstrg. h)
description: Beginnt die direkte Bearbeitung des angegebenen Texts des Listen Ansichts Elements. In der Meldung wird das angegebene Element implizit ausgewählt und fokussiert. Sie können diese Nachricht explizit oder mithilfe des ListView \_ EditLabel-Makros senden.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Windows-Steuerelemente für LVM_EDITLABEL Meldung
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
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739968"
---
# <a name="lvm_editlabel-message"></a>LVM- \_ EditLabel-Nachricht

Beginnt die direkte Bearbeitung des angegebenen Texts des Listen Ansichts Elements. In der Meldung wird das angegebene Element implizit ausgewählt und fokussiert. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements. Um die Bearbeitung abzubrechen, legen Sie den Index auf-1 fest.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungs Steuerelement zurück, mit dem der Element Text bei erfolgreicher Bearbeitung bearbeitet wird, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig. Sie können das Bearbeitungs Steuerelement unterteilen, aber Sie sollten es nicht zerstören.

Vor dem Senden dieser Nachricht an das-Steuerelement muss das-Steuerelement den Fokus haben. Der Fokus kann mithilfe der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion festgelegt werden.

Wenn *wParam* den Wert-1 hat, wird ein [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Editlabelw** (Unicode) und **LVM \_ editlabela** (ANSI)<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

