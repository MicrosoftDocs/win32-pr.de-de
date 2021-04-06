---
title: LVM_SETITEMPOSITION Meldung (kommstrg. h)
description: Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden). Sie können diese Nachricht explizit oder mithilfe des ListView-Makros "-Tabelle" senden \_ .
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Windows-Steuerelemente für LVM_SETITEMPOSITION Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858941"
---
# <a name="lvm_setitemposition-message"></a>LVM- \_ Nachricht "abtitemposition"

Verschiebt ein Element an eine angegebene Position in einem Listenansicht-Steuerelement (muss sich in der Symbol Ansicht oder in der kleinen Symbol Ansicht befinden). Sie können diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) -Makros "-Tabelle" senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die neue x-Position der oberen linken Ecke des Elements in Ansichts Koordinaten an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die neue y-Position der oberen linken Ecke des Elements in Ansichts Koordinaten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das Listenansicht-Steuerelement den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil aufweist, werden die Elemente im Listenansicht-Steuerelement nach dem Festlegen der Position des Elements angeordnet.

Unter Windows Vista führt das Senden dieser Nachricht an ein Listenansicht-Steuerelement mit dem [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil nichts aus, und der Rückgabewert ist **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

