---
title: TVM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Struktur Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ geteditcontrol-Makros senden.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Windows-Steuerelemente für TVM_GETEDITCONTROL Meldung
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105962"
---
# <a name="tvm_geteditcontrol-message"></a>TVM \_ geteditcontrol-Meldung

Ruft das Handle für das Bearbeitungs Steuerelement ab, das verwendet wird, um den Text eines Struktur Ansichts Elements zu bearbeiten. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ geteditcontrol**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Bearbeitungs Steuerelement zurück, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, aber nicht positioniert oder angezeigt. Bevor es angezeigt wird, sendet das Strukturansicht-Steuerelement seinem übergeordneten Fenster einen [TVN \_ beginlabeledit](tvn-beginlabeledit.md) -Benachrichtigungs Code.

Zum Anpassen der Bezeichnungs Bearbeitung implementieren Sie einen Handler für [TVN \_ beginlabeledit](tvn-beginlabeledit.md) und senden eine **TVM \_ geteditcontrol** -Nachricht an das Strukturansicht-Steuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement. Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





