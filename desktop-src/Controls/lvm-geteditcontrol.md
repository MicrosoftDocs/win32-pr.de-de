---
title: LVM_GETEDITCONTROL Nachricht (Commctrl.h)
description: Ruft das Handle für das Bearbeitungssteuerelement ab, das zum Bearbeiten des Texts eines Listenansichtselements verwendet wird. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetEditControl-Makros senden.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 29f7e7ac31b3d429ab32ac6564a47f859f0e5dc2207d991cb580173838a4c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968310"
---
# <a name="lvm_geteditcontrol-message"></a>LVM \_ GETEDITCONTROL-Nachricht

Ruft das Handle für das Bearbeitungssteuerelement ab, das zum Bearbeiten des Texts eines Listenansichtselements verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetEditControl-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg das Handle an das Bearbeitungssteuerelement zurück, andernfalls **NULL.**

## <a name="remarks"></a>Hinweise

Wenn die Bearbeitung von Bezeichnungen beginnt, wird ein Bearbeitungssteuerelement erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansichtssteuerelement seinem übergeordneten Fenster einen [LVN \_ BEGINLABELEDIT-Benachrichtigungscode.](lvn-beginlabeledit.md)

Implementieren Sie zum Anpassen der Bearbeitung von Bezeichnungen einen Handler für [LVN \_ BEGINLABELEDIT,](lvn-beginlabeledit.md) und senden Sie eine **LVM \_ GETEDITCONTROL-Nachricht** an das Listenansichtssteuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungssteuerelement. Verwenden Sie dieses Handle, um das Bearbeitungssteuerelement anzupassen, indem Sie die üblichen **EM \_ XXX-Nachrichten** senden.

Wenn der Benutzer die Bearbeitung abschließt oder abbricht, wird das Bearbeitungssteuerelement zerstört, und das Handle ist nicht mehr gültig. Sie können das Bearbeitungssteuerelement untergliedern, sollten es jedoch nicht zerstören. Um die Bearbeitung abzubrechen, senden Sie dem Listenansichtssteuerelement eine [**WM \_ CANCELMODE-Nachricht.**](/windows/desktop/winmsg/wm-cancelmode)

Das zu bearbeitende Listenansichtselement ist das aktuell fokussierte Element, d. h. das Element im Fokuszustand. Um ein Element basierend auf seinem Zustand zu suchen, verwenden Sie die [**LVM \_ GETNEXTITEM-Nachricht.**](lvm-getnextitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

