---
title: EM_SETMODIFY (Winuser.h)
description: Legt das Änderungsflag für ein Bearbeitungssteuerzeichen fest oder löschen es. Das Änderungsflag gibt an, ob der Text im Bearbeitungssteuerfeld geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY von Windows-Steuerelementen
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
ms.openlocfilehash: fcd367a828e7f431b6177a2ec99fe508fec3e48c4743d492277f00ed4965e001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831162"
---
# <a name="em_setmodify-message"></a>EM \_ SETMODIFY-Nachricht

Legt das Änderungsflag für ein Bearbeitungssteuerzeichen fest oder löschen es. Das Änderungsflag gibt an, ob der Text im Bearbeitungssteuerfeld geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der neue Wert für das Änderungsflag. Der Wert **TRUE gibt** an, dass der Text geändert wurde, und der Wert **FALSE** gibt an, dass er nicht geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Beim Erstellen des Steuerelements wird das Änderungsflag automatisch auf 0 (null) gelöscht. Wenn der Benutzer den Text des Steuerelements ändert, legt das System das Flag auf ungleich 0 (null) fest. Sie können die [**EM \_ GETMODIFY-Nachricht**](em-getmodify.md) an das Bearbeitungssteuerzeichen senden, um den aktuellen Status des Flags abzurufen.

**Rich Edit 1.0:** Objekte, die ohne **das REO \_ DYNAMICSIZE-Flag** erstellt wurden, sperren ihre Extent, wenn das Modify-Flag auf **FALSE festgelegt ist.**

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> <dt>

[**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





