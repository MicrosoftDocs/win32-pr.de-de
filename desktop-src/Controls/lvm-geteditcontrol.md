---
title: LVM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Listen Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des ListView \_ geteditcontrol-Makros senden.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Windows-Steuerelemente für LVM_GETEDITCONTROL Meldung
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040105"
---
# <a name="lvm_geteditcontrol-message"></a>LVM \_ geteditcontrol-Nachricht

Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Listen Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ geteditcontrol**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungs Steuerelement zurück, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement seinen übergeordneten Fenster einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Code.

Implementieren Sie zum Anpassen der Bezeichnungs Bearbeitung einen Handler für [LVN \_ beginlabeledit](lvn-beginlabeledit.md) , und senden Sie eine **LVM \_ geteditcontrol** -Nachricht an das Listenansicht-Steuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement. Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungs Steuerelement zerstört und das Handle ist nicht mehr gültig. Sie können das Bearbeitungs Steuerelement unterteilen, aber Sie sollten es nicht zerstören. Zum Abbrechen der Bearbeitung senden Sie das Listenansicht-Steuerelement an eine [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) -Meldung.

Das zu bearbeitende Listen Ansichts Element ist das aktuell fokussierte Element, d. h. das Element im Fokus Zustand. Um nach einem Element auf der Grundlage seines Zustands zu suchen, verwenden Sie die [**LVM \_ GetNextItem**](lvm-getnextitem.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListView \_ geteditcontrol**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

