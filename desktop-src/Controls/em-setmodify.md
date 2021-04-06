---
title: EM_SETMODIFY Meldung (Winuser. h)
description: Legt das Änderungsflag für ein Bearbeitungs Steuerelement fest oder löscht dieses. Das Änderungsflag gibt an, ob der Text im Bearbeitungs Steuerelement geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Windows-Steuerelemente für EM_SETMODIFY Meldung
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859012"
---
# <a name="em_setmodify-message"></a>EM- \_ setmodify-Meldung

Legt das Änderungsflag für ein Bearbeitungs Steuerelement fest oder löscht dieses. Das Änderungsflag gibt an, ob der Text im Bearbeitungs Steuerelement geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der neue Wert für das Änderungsflag. Der Wert **true** gibt an, dass der Text geändert wurde, und der Wert **false** gibt an, dass er nicht geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement erstellt wird, löscht das System das Änderungsflag automatisch auf 0 (null). Wenn der Benutzer den Text des Steuer Elements ändert, legt das System das Flag auf einen Wert ungleich 0 (null) fest. Sie können die [**EM \_ getmodify**](em-getmodify.md) -Nachricht an das Bearbeitungs Steuerelement senden, um den aktuellen Status des Flags abzurufen.

**Rich Edit 1,0:** Objekte, die ohne das **REO \_ dynamicsize** -Flag erstellt werden, Sperren Ihre Blöcke, wenn das Modify-Flag auf " **false**" festgelegt ist.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getmodify**](em-getmodify.md)
</dt> <dt>

[**Reobject**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





